# VIVES Smart Campus

http://vives-smart-campus.be

## First time setup

Start the services with the following command:

```
docker-compose up -d
```

Note that the first time you run the services, the database will be empty. A migration is needed to create all the necessary tables. Initial data can be seeded as well to get the services working correctly. This can be achieved with the following command:

```
docker-compose exec backend php artisan migrate:refresh --seed
```

## Starting and stopping

When the database (volume) is already pressent, you can start and stop the services with the following commands:

```
docker-compose start
```

```
docker-compose stop
```

## Updating services

Newer images can be downloaded with the following command:

```
docker-compose pull
```

When starting the services with `docker-compose up`, the updates will be applied.


## Secrets

Use the `.env` file to set the secrets and passwords.

* `APP_KEY` Application secret key for Laravel
* `TTN_APPID` The application ID of the Things Network Application
* `TTN_ACCESSKEY` can be found on the application page in the TTN dashboard