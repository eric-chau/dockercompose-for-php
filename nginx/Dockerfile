FROM alpine:3.18.2

RUN apk add --update --no-cache nginx

COPY nginx.conf /etc/nginx/
COPY app.conf /etc/nginx/conf.d/

RUN echo "upstream php-upstream { server php:9000; }" > /etc/nginx/conf.d/upstream.conf

CMD ["nginx"]
