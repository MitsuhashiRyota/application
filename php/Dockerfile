### Docker Image File Setting ###
FROM php:7.2-fpm

### Permission Settig ###
ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_NO_INTERACTION 1

### Install Composer Setting ###
RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer
RUN apt-get update \
&& apt-get install -y \
git \
zip \
unzip \
vim

### Install PHP Modules ###
RUN apt-get update \
    && apt-get install -y libpq-dev \
    && docker-php-ext-install pdo_mysql pdo_pgsql

## Work Directory Setting ##
WORKDIR /var/www/html/laravel
