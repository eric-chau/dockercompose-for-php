FROM alpine:3.8

RUN apk add --update --no-cache nginx

COPY nginx.conf /etc/nginx/
COPY app.conf /etc/nginx/conf.d/

RUN echo "upstream php-upstream { server php:9001; }" > /etc/nginx/conf.d/upstream.conf

CMD ["nginx"]

EXPOSE 80
EXPOSE 443
