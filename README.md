# Laravel Docker

## Versions
* Laravel Framework 8.74.0
* Composer version 2.1.14
* PHP 7.4.26
* Node v12.22.7
* Npm 6.14.15

## Installation
```
cp .env.example .env
docker-compose build app
docker-compose up -d
docker-compose exec app composer install
docker-compose exec app php artisan key:generate
docker-compose exec app php artisan migrate:fresh --seed
docker-compose exec app npm install
docker-compose exec app npm run dev 
```

## App
http://localhost:8000

## MySQL

https://hub.docker.com/_/mysql

### Se connecter au shell du container
```
docker exec -it laraveldocker-db bash
```
### Visionner les logs
```
docker logs laraveldocker-db
```

## Nginx

https://hub.docker.com/_/nginx

## Consulter les logs
### error.log
```
docker logs -f laraveldocker-nginx 1>/dev/null
```

### access.log
```
docker logs -f laraveldocker-nginx 2>/dev/null
```

### Php Myadmin
http://localhost:8080

