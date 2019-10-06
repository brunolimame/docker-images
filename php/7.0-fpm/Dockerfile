FROM phpdockerio/php7-fpm:latest
MAINTAINER eu@brunolima.me
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-mongodb php-mysql php-pgsql php-redis php-sqlite3 php-bz2 php-enchant php-gd php-geoip php-gmp php-igbinary php-imagick php-imap php-interbase php-intl php-ldap php-odbc php-phpdbg php-pspell php-recode php-snmp php-soap php-ssh2 php-xdebug php-xmlrpc php-xsl \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*