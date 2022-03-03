FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
    libzip-dev \
    libonig-dev

RUN docker-php-ext-install \
    zip \
    pdo_mysql \
    mbstring opcache

WORKDIR /var/www
