FROM php:8.1-fpm-buster
RUN pecl install xdebug \
    && docker-php-ext-enable xdebug
RUN apt-get update
RUN apt-get install -y git libzip-dev vim libpng-dev

RUN apt-get update && apt-get install -y zlib1g-dev

RUN docker-php-ext-install zip
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install gd
RUN docker-php-ext-enable gd

RUN printf '[PHP]\ndate.timezone = "Pacific/Auckland"\n' > /usr/local/etc/php/conf.d/tzone.ini
COPY ./docker/php/uploads.ini /usr/local/etc/php/conf.d/uploads.ini
