FROM php:7-apache


## Update packages
RUN apt-get update

## Install depending packages
RUN apt-get install -y --no-install-recommends \
wget \
libmcrypt-dev

## Install FuelPHP's depending extensions
RUN docker-php-ext-install \
fileinfo \
mbstring \
mcrypt

## Cleanup
RUN rm -rf /var/lib/apt/lists/*

## Set php.ini
RUN cat /usr/src/php/php.ini-development | sed 's/^;\(date.timezone.*\)/\1 \"Asia\/Tokyo\"/' > /usr/local/etc/php/php.ini

## TODO: Install xdebug

## Install phpunit
RUN wget https://phar.phpunit.de/phpunit.phar
RUN chmod +x phpunit.phar
RUN mv phpunit.phar /usr/local/bin/phpunit

## Enable mod_rewrite
RUN a2enmod rewrite

## Restart Apache
RUN service apache2 restart
