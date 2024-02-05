
ARG PHP_IMAGE_VERSION
ARG PHP_IMAGE=php:${PHP_IMAGE_VERSION}


FROM ${PHP_IMAGE}

RUN apk update && apk add --no-cache \
  vim \
  libzip-dev \
  unzip \
  bash \
  linux-headers

# Install PHP Extensions
RUN docker-php-ext-install zip \
  && docker-php-ext-install sockets \
  && docker-php-ext-install opcache \
  && docker-php-ext-enable opcache

# Copy Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer
WORKDIR '/app'

CMD ["/app/rr", "serve", "-d", "-c", ".rr.yaml"]
