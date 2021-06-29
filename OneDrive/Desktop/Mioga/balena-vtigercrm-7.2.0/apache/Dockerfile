ARG APACHE_VERSION="2.4.32"
FROM httpd:2.4.32-alpine

RUN apk update; \
    apk upgrade;

# Copy apache vhost file to proxy php requests to php-fpm container
RUN mkdir -p /usr/local/apache2/conf;
ADD vtiger7.apache.conf /usr/local/apache2/conf/vtiger7.apache.conf
# Copy ssl files to proxy php requests to php-fpm container

RUN echo "Include /usr/local/apache2/conf/vtiger7.apache.conf" \
    >> /usr/local/apache2/conf/httpd.conf

VOLUME /var/www/html
    

