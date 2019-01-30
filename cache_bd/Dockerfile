FROM debian:stretch

RUN apt update \
 && apt upgrade -y
RUN apt install varnish -y

ADD src/default.vcl /etc/varnish/default.vcl
ADD src/varnish /etc/default/varnish
