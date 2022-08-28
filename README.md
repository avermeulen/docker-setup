# Docker setup


```
docker run --rm --name mongodb -v ~/docker/volumes/mongo/data:/data/db -d  -p   27017:27017 mongo:latest
docker run --rm --name pg-docker -e POSTGRES_PASSWORD=docker -d -p 5432:5432 -v $HOME/docker/volumes/postgres:/var/lib/postgresql/data postgres
docker run --rm --name 9-bullseye  -e POSTGRES_PASSWORD=docker -d -p 5432:5432 -v $HOME/docker/volumes/postgres9:/var/lib/postgresql/data postgres:9-bullseye
```

## connect to pg running on Docker

```
psql -h localhost -p 5432 -U postgres
```

## pg setup


```
CREATE USER avos WITH PASSWORD 'avos123';
GRANT ALL PRIVILEGES ON DATABASE "avo_shopper" to avos;
```
