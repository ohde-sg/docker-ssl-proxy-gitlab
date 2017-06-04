FROM php:5.6.20-apache

RUN apt-get update && apt-get install -y ssl-cert \
  --no-install-recommends && rm -r /var/lib/apt/lists/*
# rewriteモジュールを有効にする
RUN a2enmod rewrite
RUN a2enmod proxy
RUN a2enmod proxy_http
RUN a2enmod ssl

#COPY ssl-default.conf /etc/apache2/sites-enabled/

WORKDIR /var/www/html
