# hfjv_docker

Docker version of the [High Frequency Jet Ventlation Database](https://github.com/rikthomas/hfjv) for the EMAP project

## Installation

Tested on Ubuntu 18.04

- Clone repository
- `cd laradock`
- `cp env-example .env`
- Open the `docker-compose.yml` and change port numbers etc.
- `docker-compose up -d nginx mysql`
- Wait for about 15 minutes
- `docker-compose exec workspace bash`
- `composer install`
- `cp env-example .env`
- `artisan key:generate`
- `exit`
- `cd ..`
- `sudo chmod -R 777 storage bootstrap/cache`
- `docker-compose exec workspace bash`
- `artisan migrate`
- `exit`
