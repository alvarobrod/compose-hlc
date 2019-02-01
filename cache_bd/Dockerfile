FROM debian:stretch

RUN apt update \
 && apt upgrade -y
RUN apt install varnish -y

COPY src/default.vcl /etc/varnish/default.vcl
COPY src/varnish /etc/default/varnish
