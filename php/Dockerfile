FROM php:latest
RUN apt update && apt install wget -y
RUN wget https://raw.githubusercontent.com/php/php-src/PHP-7.2.2/php.ini-development /usr/local/etc/php/php.ini
RUN echo -e "extension=swoole.so\extension=redis.so" >> /usr/local/etc/php/php.ini
RUN pecl install swoole redis
RUN cd /usr/local/bin && wget https://getcomposer.org/composer.phar
RUN chmod a+x composer.phar && mv composer.phar /usr/local/bin/composer 
RUN composer.phar self-update && composer self-update