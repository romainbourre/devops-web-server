FROM nginx:latest

RUN apt-get update

RUN apt-get install -y \
    certbot \
    python-certbot-nginx\
    vim

COPY ./conf/nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./conf/nginx/conf.d /etc/nginx/conf.d

VOLUME /etc/nginx
VOLUME /etc/ssl/private

EXPOSE 80
EXPOSE 443
