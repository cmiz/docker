FROM php:8.4-fpm

ARG HOST_UID
ARG HOST_GID

RUN usermod --uid ${HOST_UID} www-data && groupmod --gid ${HOST_GID} www-data

RUN apt-get update \
    && apt-get install -y \
    libzip-dev \
    libpng-dev \
    libonig-dev \
    curl \
    unzip \
    default-mysql-client

RUN pecl install xdebug && docker-php-ext-enable xdebug

RUN docker-php-ext-install \
    gd \
    zip \
    pdo_mysql \
    mbstring \
    opcache \
    bcmath

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN chown -R www-data:www-data /var/www

USER www-data

ENV PATH="${PATH}:/var/www/.composer/vendor/bin"

RUN composer global require laravel/installer

WORKDIR /var/www/html
