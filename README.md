# Dockerize PHP develop
Docker compose to setup nginx, php and mysql for PHP develop   

## Directory Structure
```sh
.
├── mysql
├── nginx
├── php
├── var/www/html/
└── docker-compose.yml

```
## Images
1. nginx → nginx:latest
2. php → php:7.4-fpm
3. mysql → mysql:5.7

## Setup Initial DB  
Copy your sql file to *docker/mysql* with *based.sql* as a file name.  

## Deployment using Docker
1. Deploy nginx, php-fpm, and mysql using docker-compose
    ```bash
    docker-compose up -d
    ```
2. Stop all container
    ```bash
    docker stop nginx mysql5.7 PHP7.4
    ```
3. Remove all container
    ```bash
    docker rm nginx mysql5.7 PHP7.4
    ```
4. Reset mysql data
    ```bash
    bash reset-db.sh
    ```
