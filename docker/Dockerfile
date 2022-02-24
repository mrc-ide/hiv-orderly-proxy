FROM reside/proxy-nginx:latest

RUN apt-get update && apt-get install -y patch

COPY nginx.conf.patch /etc/nginx/nginx.conf.patch
RUN patch --dry-run /etc/nginx/nginx.conf.template /etc/nginx/nginx.conf.patch

## Add custom static site
COPY src/ /usr/share/nginx/html/