## AWS IAM (Identity and Access Management)
```
IAM is the AWS service used to control who can access AWS resources and what actions they are allowed to perform.
```

## Crisp explanation
```
AWS IAM is a global AWS service that manages authentication and authorization.
It allows you to create users, groups, and roles, and attach policies to define what actions they can perform on AWS resources.
```
## Breakdown 

```
User → An individual identity (person or application).

Group → Collection of users with the same permissions.

Role → Temporary identity assumed by services or users.

Policy → JSON document defining permissions (Allow/Deny actions on resources).
```

## One simple example
``
A developer needs to upload files to S3 but should not delete buckets.

You create:

IAM User → dev-user

Attach Policy → Allow s3:PutObject

Deny or avoid s3:DeleteBucket

Now that user can upload objects but cannot delete the bucket.

One strong interview line (use this):

IAM controls access to AWS resources using identities (users, roles) and permission policies.

```