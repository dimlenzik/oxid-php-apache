Extended PHP base container
===========================

Based on the images provided at https://hub.docker.com/_/php.

Changes contain:
- Installing necessary PHP-extensions
- Use of msmtp for sendmail
- Removing memory limits on PHP
- Installing Xdebug and provide an option to enable it
- Installing Composer

To build locally use ./build.sh [Major].[Minor] a.e. `./build.sh 7.1`

Danach aus dem Oxid-Base-Verzeichnis:
docker run --rm -ti -v "${PWD}:/var/www/html/shop:cached" -p 8080:80 oxidesales/oxideshop-docker-php:7.4 bash

In der Bash "apache2ctl start"

MySQL:
docker run --rm -ti --name oxid_coding_days_mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password -d mysql:latest
