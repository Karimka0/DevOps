FROM alpine:latest

ARG PORT=80

RUN apk update && \
    apk add --no-cache nginx

WORKDIR /var/www/html

EXPOSE $PORT

RUN chown -R nginx:nginx /var/www/html

VOLUME ["/var/www/html"]
USER nginx

CMD ["nginx", "-g", "daemon off;"]
