FROM php:7.1-fpm
MAINTAINER eu@brunolima.me

RUN apt-get update && apt-get -y upgrade && apt-get -y dist-upgrade
RUN apt-get install -y vim
# Some basic extensions
RUN docker-php-ext-install -j$(nproc) json mbstring pdo pdo_mysql mysqli

# Curl
RUN apt-get install -y libcurl4-openssl-dev
RUN docker-php-ext-install -j$(nproc) curl

# GD
RUN apt-get install -y libpng-dev libjpeg-dev
RUN docker-php-ext-install -j$(nproc) gd

# Intl
RUN apt-get install -y libicu-dev
RUN docker-php-ext-install -j$(nproc) intl


