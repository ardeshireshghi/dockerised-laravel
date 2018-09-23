FROM php:7.2-fpm

# Install composer
RUN php -r "readfile('https://getcomposer.org/installer');" | php && \
   mv composer.phar /usr/bin/composer && \
   chmod +x /usr/bin/composer

RUN apt-get update && apt-get install -y git zip unzip

WORKDIR /data

COPY fpm-log.conf /usr/local/etc/php-fpm.d/zz-log.conf
