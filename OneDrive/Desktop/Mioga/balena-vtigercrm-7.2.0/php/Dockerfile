ARG PHP_VERSION="7.4"
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm-alpine

RUN apk update \
    apk upgrade

ADD https://sourceforge.net/projects/vtigercrm/files/vtiger%20CRM%206.5.0/Core%20Product/vtigercrm6.5.0.tar.gz/download /var/www/html/vtigercrm6.5.0.tar.gz
RUN cd /var/www/html && tar xvfz vtigercrm6.5.0.tar.gz

RUN chown -R www-data /var/www/html && \
    chgrp -R www-data /var/www/html && \
    chmod -R 0755 /var/www/html;




VOLUME /var/www/html
