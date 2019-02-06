FROM debian:stretch
RUN apt update \
 && apt upgrade -y
RUN apt install apache2 -y && apt install wget -y && apt install unzip -y

EXPOSE 80

RUN mkdir /var/www/prestashop
RUN chown -R www-data. /var/www/prestashop

RUN wget https://download.prestashop.com/download/releases/prestashop_1.7.2.4.zip
RUN unzip prestashop_1.7.2.4.zip
RUN mv prestashop.zip /var/www/prestashop
RUN mv index.php /var/www/prestashop

ADD prestashop.conf /etc/apache2/sites-enabled/000-default.conf

CMD apachectl -D FOREGROUND

