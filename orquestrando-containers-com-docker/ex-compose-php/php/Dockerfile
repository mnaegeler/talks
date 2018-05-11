FROM php:7.0-fpm

MAINTAINER andreluizleoni@gmail.com

WORKDIR /var/www/html

COPY config/php.ini /usr/local/etc/php/

RUN docker-php-ext-install pdo pdo_mysql mysqli
