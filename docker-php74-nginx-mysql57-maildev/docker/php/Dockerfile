FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
    libzip-dev \
    libpng-dev \
    libonig-dev

RUN docker-php-ext-install \
    gd \
    zip \
    pdo_mysql \
    mbstring \
    opcache

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /var/www
