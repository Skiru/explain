FROM php:7.4-fpm

RUN apt-get update \
    && apt-get install -y libicu-dev libzip-dev zip git g++ \
    && docker-php-ext-install intl zip pdo pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer creates=/usr/local/bin/composer warn=no