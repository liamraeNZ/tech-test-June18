FROM alpine:latest
RUN apk add --update nginx && rm -rf /var/cache/apk/*

COPY default.conf /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/nginx.conf
COPY test-site/ /var/www/html/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]