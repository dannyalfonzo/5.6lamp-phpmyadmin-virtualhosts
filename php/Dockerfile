FROM php:5.6.36-apache	
# php:7.1-apache or php:7.0-apache, php:5.6-apache @see https://github.com/docker-library/php

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/ssl-cert-snakeoil.key -out /etc/ssl/certs/ssl-cert-snakeoil.pem -subj "/C=AT/ST=Vienna/L=Vienna/O=Security/OU=Development/CN=example.com"
RUN a2enmod ssl

RUN a2enmod rewrite

RUN apt-get update

RUN apt-get install libcurl3-dev libpng-dev libmcrypt-dev libxml2-dev -y

RUN docker-php-ext-install mysqli pdo pdo_mysql curl gd mbstring gettext mcrypt xmlrpc soap intl zip xml calendar


