# Notes for Contributors
First of all thank you for providing a helping hand into out efforts.

## Docker files
As you noticed there are the following `docker-compose.yml` files:

* The `docker-compose-alpine-fpm.yml` used in testing the alpine based images.
* The `docker-compose-apache.yml` Used in testing the apacke-based-images.
* Τhe `docker-compose-ssl-reverse-nginx.yml` used for testing the moodle's behavior againist a nginx reverse proxy.

## Something wrong happens during container launch:
Then run the following commands:

```
docker-compose -f ^yml file^ down -v --remove-orphans
docker-compose down -v --remove-orphans
```
## Ressetting the installation
Run the same commands as above.

## HTTP timeout
Also in case of an arror that mentions:

```
UnixHTTPConnectionPool(host='localhost', port=None): Read timed out. (read timeout=60)
```

Export the following enviromental variables:

```
export DOCKER_CLIENT_TIMEOUT=120
export COMPOSE_HTTP_TIMEOUT=120
```

## Continuous Integration

The Continious Integration (eg. travis-ci) requires the following secret values to be set into as enviromental variables in order to deploy:
- `DOCKER_USER` That contains a docker hub user (that has access to the org's repository)
- `DOCKER_TOKEN` A secret access token used in order to deploy into docker hub.
