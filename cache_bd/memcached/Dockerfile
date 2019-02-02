FROM debian:stretch

RUN apt update \
 && apt upgrade -y
RUN apt install php7.0 memcached php-pear pkg-config zlib1g-dev libmemcached-dev -y
RUN pecl install memcached
