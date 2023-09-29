Assignment2: Extend Docker Image with AWS SDK

To extend an existing Docker image and install the AWS SDK, we can create a new Dockerfile:
Dockerfile:
# syntax=docker/dockerfile:2

FROM node:18-alpine
FROM amazon/aws-cli
WORKDIR /app
COPY . .
RUN yarn install --production
RUN npm install -g aws-sdk
CMD ["node", "src/index.js"]
EXPOSE 3000


# Build the Docker image:
docker build -t getting-started-image2 .

# Run the Docker container from the image:
docker run -dp 127.0.0.1:3000:3000 getting-started2