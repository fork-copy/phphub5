FROM hellomjw/php:5.6_v1.0.1
RUN apk add --no-cache --virtual .build-deps \
    g++ make autoconf
RUN pecl install -o -f redis \
&&  rm -rf /tmp/pear \
&&  echo "extension=redis.so" > /usr/local/etc/php/conf.d/redis.ini
RUN apk del --purge .build-deps
