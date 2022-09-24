FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
	&& docker-php-ext-install mysqli

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html