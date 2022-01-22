FROM php:8-fpm

COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -

RUN apt-get update && \
    apt-get install -y libzip-dev libonig-dev nodejs && \
    docker-php-ext-install zip pdo_mysql mbstring opcache

WORKDIR /var/www
