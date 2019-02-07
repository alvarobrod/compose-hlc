FROM debian:stretch

RUN apt-get -y update && apt upgrade -y && apt dist-upgrade -y
RUN apt install php7.0 php7.0-fpm php7.0-memcached php7.0-curl php7.0-mysql php7.0-zip php7.0-simplexml -y

RUN sed -ri 's/^listen.*/listen=ip_phpfmp:9000/' /etc/php/7.0/fpm/pool.d/www.conf

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

EXPOSE 9000

CMD ["php-fpm7.0"]
