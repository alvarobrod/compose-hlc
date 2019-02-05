FROM debian:stretch

RUN set -ex; \
 apt update; \
 apt upgrade -y
RUN apt install memcached php-memcached -y

COPY src/memcached.conf /etc/memcached.conf
