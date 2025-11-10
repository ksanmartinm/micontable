FROM php:8.3-cli

# Instalar dependencias
RUN apt-get update && apt-get install -y \
    git curl vim zip unzip libzip-dev libpng-dev libjpeg-dev libfreetype6-dev \
    && docker-php-ext-install pdo_mysql gd zip

# Instalar Composer globalmente
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

WORKDIR /var/www
