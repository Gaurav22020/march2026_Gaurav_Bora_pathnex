## VPC (Virtual Private Cloud)
```
Definition (crisp):

A VPC is a logically isolated virtual network in AWS where you launch and manage your cloud resources.

Think of it as your private data center network inside AWS.

Inside a VPC you control:

IP address range (CIDR block)

Subnets

Route tables

Internet access

Security rules

Example:

VPC: 10.0.0.0/16
   ├── Public Subnet (10.0.1.0/24)
   └── Private Subnet (10.0.2.0/24)

```

## Key components inside VPC:
```
Subnets → network segments

Route Tables → control traffic routing

Internet Gateway → internet access

NAT Gateway → private subnet internet access

Security Groups → instance firewall

NACL → subnet-level firewall

```

## Interview line
```
A VPC provides network isolation and allows you to define your own IP addressing, routing, and security within AWS.
```