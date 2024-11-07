## Containerize Your Application
## Build and Test Locally
```bash
docker build -t my-python-app .
docker run -p 5000:5000 my-python-app
```

## Push Docker Image to Amazon ECR
```bash
aws ecr create-repository --repository-name my-python-app
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.us-east-1.amazonaws.com
docker tag my-python-app:latest <aws_account_id>.dkr.ecr.us-east-1.amazonaws.com/my-python-app:latest
docker push <aws_account_id>.dkr.ecr.us-east-1.amazonaws.com/my-python-app:latest
```

## Set Up ECS Cluster and Task Definition

## Create a Service

## Access Application

