FROM nginx:latest

RUN apt-get update

RUN apt-get install -y \
    certbot \
    python-certbot-nginx\
    vim

COPY ./src /usr/share/nginx/html
COPY ./conf/nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./conf/nginx/conf.d /etc/nginx/conf.d

WORKDIR /etc/nginx

VOLUME /usr/share/nginx/html
VOLUME /etc/nginx
VOLUME /etc/ssl/private

EXPOSE 80
EXPOSE 443
