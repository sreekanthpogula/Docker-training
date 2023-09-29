Assignment3: Create Docker Containers for Web App and DB

I have a web application and a persistence database
# create a docker-compose.yml file:
version: '3'
services:
  webapp:
    image: your-webapp-image
    ports:
      - "8080:80" # Adjust the port as needed
    depends_on:
      - db

  db:
    image: your-db-image
    environment:
      MYSQL_ROOT_PASSWORD: example
      MYSQL_DATABASE: your-database-name
Then, use the following commands to build and run the containers:

# build
docker-compose build

# run
docker-compose up -d

Ensure that your web application code connects to the database using the container name "db" as the hostname.