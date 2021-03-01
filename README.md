# pgadmin4
pgadmin4 is a Pgadmin4 web server, that serve as postgresql web server for [postgres_server](https://github.com/BorodaUA/postgres_server). And it is a part of the [webportal](https://github.com/BorodaUA/webportal) project.

## How to use:
### Local development mode:
1. Clone the repo
2. Create .env file inside the repo with following data:
    - PGADMIN_LISTEN_PORT=number of the port, that Pgadmin4 will be available on
    - PGADMIN_DEFAULT_EMAIL=admin email
    - PGADMIN_DEFAULT_PASSWORD=admin password