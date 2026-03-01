# Day 1

## Kubernetes Deployment script
```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
  namespace: my-apps
spec:
  replicas: 3
  selector:
    matchLabels:
      app: myapp

  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
        - name: myapp
          image: nginx:1.25
          ports:
            - containerPort: 80
```

# Service
```
apiVersion: v1
kind: Service
metadata:
  name: my-app-service
spec:
  type: ClusterIP        # default
  selector:
    app: my-app          # MUST match pod labels
  ports:
    - port: 80           # service port
      targetPort: 8080   # container port
```

## Terraform
```
terraform{
  required_providers{
    azurerm ={
      source="hashicorp/azurerm"
      version="~>4.53"
    }
  }
}
provider "azurerm"{
  features{}
}


resource"azurerm_resource_group" "RG"{
  name="MyRg"
  location="central india"
}

```

## Jenkins

```
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/user/repo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }
    }
}
```