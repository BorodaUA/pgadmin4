# pgadmin4
pgadmin4 is a Pgadmin4 web server, that serve as postgresql web server for [postgres_server](https://github.com/BorodaUA/postgres_server). And it is a part of the [webportal](https://github.com/BorodaUA/webportal) project.

## How to use:
### Local development mode:
1. Clone the repo
2. Create .env file inside the repo with following data:
    - PGADMIN_LISTEN_PORT=number of the port, that Pgadmin4 will be available on
    - PGADMIN_DEFAULT_EMAIL=admin email
    - PGADMIN_DEFAULT_PASSWORD=admin password
## Run as separate container:
1. Create Docker image for the project
```
docker build -t ${PWD##*/}-image .
```
2. Run project's Docker container
```
docker run -d -p 7000:7000 --env-file .env --link postgres --name ${PWD##*/}-container ${PWD##*/}-image
```
3. Stop and remove project's Docker container
```
docker rm -f ${PWD##*/}-container
```
4. Remove project's Docker image
```
docker image rm -f ${PWD##*/}-image
```
### .env files setup:
1. In project's main folder create .env files out of .env.example files
```
.env
.env.example
```
