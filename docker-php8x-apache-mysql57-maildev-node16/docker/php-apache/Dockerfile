FROM php:8-apache

COPY *.conf /etc/apache2/sites-enabled/
COPY php.ini /usr/local/etc/php/

RUN a2enmod ssl && a2enmod rewrite

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -

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

RUN openssl req -new -newkey rsa:4096 -days 365 -nodes -x509 \
    -subj "/C=JP/CN=local.test.site" \
    -keyout /etc/apache2/ssl-server.key \
    -out /etc/apache2/ssl-server.crt

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /var/www
