FROM debian:stretch

RUN set -ex; \
 apt update; \
 apt upgrade -y
RUN apt install memcached -y

EXPOSE 11211

CMD memcached -l 0.0.0.0 -u memcache
