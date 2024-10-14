# docker/php/Dockerfile

FROM php:8.1-fpm

# Install extentions connect between php and mysql
RUN apt-get update

RUN docker-php-ext-install pdo pdo_mysql mysqli

# Install extentions connect between php and mongodb
RUN apt-get install -y autoconf pkg-config libssl-dev

RUN pecl install mongodb

RUN echo "extension=mongodb.so" >> /usr/local/etc/php/conf.d/mongodb.ini