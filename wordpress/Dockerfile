FROM php:7.3-apache
RUN sh -c 'set -eux; apt-get update; apt-get install -y libzip-dev zlib1g-dev; docker-php-ext-install zip; docker-php-ext-install mysqli'
COPY php.ini /usr/local/etc/php/php.ini
COPY --chown=www-data dupinstall/ /var/www/html/
RUN a2enmod rewrite
RUN service apache2 restart
COPY mod_rewrite.conf /etc/apache2/conf-enabled/
