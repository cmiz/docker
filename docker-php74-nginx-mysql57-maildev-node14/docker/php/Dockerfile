FROM php:7.4-fpm

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -

RUN apt-get update && apt-get install -y \
    libzip-dev \
    libpng-dev \
    libonig-dev \
    nodejs \
    git

RUN docker-php-ext-install \
    gd \
    zip \
    pdo_mysql \
    mbstring \
    opcache

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /var/www
