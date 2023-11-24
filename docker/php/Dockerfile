# syntax=docker/dockerfile:1
FROM php:8.1-apache

# make some stuff
RUN apt-get update
RUN apt-get install -y --no-install-recommends nano

# we get a tool used to easily install a PHP extension
ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

# and run it
RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions amqp gd exif intl mbstring opcache pdo_mysql pdo_pgsql redis xdebug xsl zip && \
    install-php-extensions @composer

# add symfony-cli repo
RUN curl -1sLf 'https://dl.cloudsmith.io/public/symfony/stable/setup.deb.sh' | bash

# and install it
RUN apt-get install -y --no-install-recommends symfony-cli

