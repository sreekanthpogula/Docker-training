Assignment1: Create Docker Image for a Sample Application

create a Docker image for it:

Create a Dockerfile in the "getting-started" directory:
Dockerfile code:
# syntax=docker/dockerfile:1

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000


# Build the Docker image:
docker build -t getting-started-image .

# Run the Docker container from the image:
docker run -dp 127.0.0.1:3000:3000 getting-started