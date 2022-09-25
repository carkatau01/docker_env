FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
	&& docker-php-ext-install mysqli \
    && apt-get install -y libzip-dev \
    && docker-php-ext-install zip

RUN ["apt-get", "install", "-y", "zip"]
RUN ["apt-get", "install", "-y", "unzip"]

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www