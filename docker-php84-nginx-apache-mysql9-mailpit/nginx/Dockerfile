FROM nginx:stable

RUN openssl req -new -newkey rsa:4096 -days 365 -nodes -x509 \
    -subj "/C=JP/CN=localhost" \
    -keyout /etc/nginx/ssl-server.key \
    -out /etc/nginx/ssl-server.crt

WORKDIR /var/www/laravel
