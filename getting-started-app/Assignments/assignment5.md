Assignment5: Build and Push Docker Image

To build a Docker image and push it to a Docker repository (e.g., AWS ECR):

Build the Docker image as shown in Assignment 1.

# Tag the image with the ECR repository URI:
docker tag sample-app-image:latest <aws_account_id>.dkr.ecr.<region>.amazonaws.com/sample-app-repo:latest

# Log in to your ECR repository:
aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.<region>.amazonaws.com

# Push the image to ECR:
docker push <aws_account_id>.dkr.ecr.<region>.amazonaws.com/sample-app-repo:latest
