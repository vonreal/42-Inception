# 1. Set base image
FROM debian:buster

# 2. Download in APT
RUN apt update && apt install mariadb-server -y

# 3. Port number the container should expose
EXPOSE 3306

# 4. Run command in foreground of the container
CMD mysqld_safe;
