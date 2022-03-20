FROM php:7.3.32-apache

RUN sed -ri -e 's!/var/www/html!/var/www/mycode!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/!/var/www/mycode!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf

RUN apt-get update && apt-get install -y git zip unzip libfreetype6-dev libjpeg62-turbo-dev libpng16-16

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ 
RUN docker-php-ext-install pdo pdo_mysql mysqli gd

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer

RUN a2enmod rewrite

WORKDIR /var/www/mycode