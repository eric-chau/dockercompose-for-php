FROM php:8.2.8-fpm-alpine3.18

COPY --from=composer:2.5.8 /usr/bin/composer /usr/bin/composer

RUN apk add --no-cache icu-dev git zlib-dev pcre-dev ${PHPIZE_DEPS} \
    && docker-php-ext-install opcache intl  \
    && pecl install -o -f apcu-5.1.22 redis \
    && docker-php-ext-enable apcu redis.so \
    && apk del pcre-dev ${PHPIZE_DEPS}

WORKDIR /var/www/app
