FROM debian:stretch

RUN apt-get -y update && apt upgrade -y && apt dist-upgrade -y
RUN apt-get -y install php7.0-fpm php7.0-mysql php7.0-gd php7.0-memcached

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

RUN sed -ri 's/^listen.=.*/listen=172.17.0.3:9000/' /etc/php/7.0/fpm/pool.d/www.conf

CMD ["php7.0-fpm"]
