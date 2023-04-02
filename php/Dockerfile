FROM php:7.4-fpm

ENV TZ Asia/Tokyo

COPY . /var/www/html

WORKDIR /var/www/html

RUN apt-get update && \
    apt-get install -y \
    git \
    zip \
    curl

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install mysqli

COPY ./php/php.ini /usr/local/etc/php/php.ini

COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

EXPOSE 9000
CMD ["php-fpm"]
