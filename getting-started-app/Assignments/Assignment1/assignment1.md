# Assignment1

create a Docker image for getting-started application:
Create a Dockerfile in the "getting-started" directory:

1. Dockerfile code

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
2. Build the Docker image

```docker build -t getting-started-image .```
3. Run the Docker container from the image

```docker run -dp 127.0.0.1:3000:3000 getting-started```
