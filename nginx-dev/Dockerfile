FROM nginx:1.9
MAINTAINER Duane Leem <duaneleem@alumni.ggu.edu>

## Install tools.
RUN apt-get update && apt-get install -y \
    nano \
    php5-fpm \
    php5-mysql

## NGINX & PHP configurations
COPY "./artifacts/nginx/nginx.conf" "/etc/nginx/nginx.conf"
COPY "./artifacts/nginx/default.conf" "/etc/nginx/conf.d/default.conf"
COPY "./artifacts/php-fpm/php.ini" "/etc/php5/fpm/php.ini"

## Startup Script
RUN mkdir -p /etc/service/nginx
ADD ./artifacts/start.sh /etc/service/nginx/run
RUN chmod +x /etc/service/nginx/run

## Required to use nano.
ENV TERM xterm

## Port configurations.
EXPOSE 80 443
