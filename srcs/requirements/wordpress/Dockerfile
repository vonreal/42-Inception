# 1. Set base image
FROM debian:buster

# 2. Download in APT
RUN apt update && apt install -y \
    php-fpm \
    php-mysql

COPY ./conf/www.conf /etc/php/7.3/fpm/pool.d/www.conf

EXPOSE 9000

CMD service php7.3-fpm start; \
    tail -f /dev/null
