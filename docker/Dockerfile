FROM reside/proxy-nginx:latest

RUN apt-get update && apt-get install -y patch

COPY nginx.conf.patch /etc/nginx/nginx.conf.patch
RUN patch /etc/nginx/nginx.conf.template /etc/nginx/nginx.conf.patch
