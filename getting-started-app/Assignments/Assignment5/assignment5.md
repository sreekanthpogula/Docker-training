# Assignment5

Build and Push Docker Image

To build a Docker image and push it to a Docker repository(ECR)

1. Build the Docker image using
```docker build -t getting-started-image .```

2. Tag the image with the ECR repository URI:
```docker tag getting-started-image:latest <aws_account_id>.dkr.ecr.<region>.amazonaws.com/sample-app-repo:latest```

3. Log in to your ECR repository:
```aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.<region>.amazonaws.com```

4. Push the image to ECR:
```docker push <aws_account_id>.dkr.ecr.<region>.amazonaws.com/sample-app-repo:latest```
