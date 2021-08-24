# 1. Set base image
FROM debian:buster

# 2. Download in APT
RUN apt update && apt install -y \
    mariadb-server \
    procps

# 3. Port number the container should expose
EXPOSE 3306

# 4. Copy host file into a  container
COPY ./conf/50-server.cnf /etc/mysql/mariadb.conf.d/

# 5. Run command in foreground of the container
CMD service mysql start; \
    echo "CREATE DATABASE IF NOT EXISTS wordpress;" | mysql -u root --skip-password; \
    echo "CREATE USER IF NOT EXISTS 'jna'@'%' IDENTIFIED BY 'jna';" | mysql -u root --skip-password; \
    echo "GRANT ALL PRIVILEGES ON wordpress.* TO 'jna'@'%' WITH GRANT OPTION;" | mysql -u root --skip-password; \
    tail -f /dev/null
