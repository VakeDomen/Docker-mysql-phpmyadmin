# Mysql-phpmyadmin with Traefik
Docker-compose for mysql database with phpmyadmin. The dockerfiles work with traefik reverse-proxy. My tls resolver is named `le` and should be renamed if the traefik configuration is set otherwise. Same goes for entrypoints.
## Setup the environment 
To run the docker-compose file, first rename the `.env.sample` file to `.env`.
Then open the `.env` file and fill the required environment variables:

```
MYSQL_DOMAIN=
PHPMYADMIN_DOMAIN=
MYSQL_USER=
MYSQL_PASSWORD=
MYSQL_ROOT_PASSWORD=
```
Traefik will bind mysql databse to the domain specified in `MYSQL_DOMAIN` and phpmyadmin to the domain specified to `PHPMYADMIN_DOMAIN`.
## Running the docker-compose
Once the environment variables have been set, the file can be run with
```
docker-compose up -d
```
