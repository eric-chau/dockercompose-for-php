# docker-compose for PHP

This is a bootstrap for PHP (v7.3.x) development with Docker. Your source code must live inside `app/` folder.

It also install MySQL and nginx. You must edit `nginx/app.conf` to customize the virtualhost for your needs.

`symfony/var-dumper` is available for php-fpm and php-cli.
