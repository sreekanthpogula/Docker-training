# Assignment3

Create Docker Containers for Web App and DB

I have a web application with a postgres database

1. Build the Docker image of web application

```docker build -t web-app .```

2. Build the Docker image for Postgres database

```docker build -t postgres-database .```

3. define the app image
 ```docker build -t app-image```

4. define the docker-compose.yml file fo rthe application and the database configuration

5. Build the application
 ```docker-compose build```

6. run the application
 ```docker-compose up -d```
