FROM nginx

COPY default.conf /etc/nginx/conf.d/

RUN openssl req -new -newkey rsa:4096 -days 365 -nodes -x509 \
    -subj "/C=JP/CN=local.test.site" \
    -keyout /etc/nginx/ssl-server.key \
    -out /etc/nginx/ssl-server.crt

WORKDIR /var/www
