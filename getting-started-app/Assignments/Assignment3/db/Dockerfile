postgres:
restart: always
image: postgres:10
environment:
- POSTGRES_USER=${USER}
- POSTGRES_PASSWORD=${PASSWORD}
- POSTGRES_DB=${DB}
volumes:
- ./postgres-data/postgres:/var/lib/postgresql/data
ports:
- "5432:5432"