# 1. Set base image
FROM debian:buster

# 2. Update APT and Install Nginx
RUN apt update && apt -y install \
    nginx \
    openssl

# 3. CSR and Key Create
RUN openssl req -newkey rsa:2048 -nodes -x509 -subj "/C=KR/ST=Seoul/L=Seoul/O=42Seoul/CN=jna" -keyout /etc/ssl/private/jna.42.fr.key -out /etc/ssl/certs/jna.42.fr.crt

# 4. Copy host file into a  container
COPY ./conf/default /etc/nginx/sites-available/default

# 5. Port number the container should exposels
EXPOSE 443

# 6. Run command in foreground of the container
CMD ["nginx", "-g", "daemon off;"]