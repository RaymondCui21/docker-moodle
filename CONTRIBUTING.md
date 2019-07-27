# Notes for Contributors:

# For docker-compose.yml
For each purpoce in the folder `./compose` are located all `docker-compose.yml` files. On the folder `latest` are the docker-compose files are the `docker-compose.yml` for the latest moodle version whilst in the `lts` will contain the `docker-compose.yml` for the lts version of it. Either in `lts` folder or in `latest` folder the following `docker-compose.yml` folders will be contained:

Compose File | Puproce
--- | ---
`docker-compose-latest-alpine-fpm.yml` | For building the images based upon alpine php images.
`docker-compose-latest-apache.yml` | For apache based variants
`docker-compose-ssl-reverse-nginx.yml` | For testing the nginx as SSL reverse proxy.
