`git clone https://github.com/dimlen/oxid-php-apache.git`

`cd oxid-php-apache`

`./build.sh 7.4`

`docker run --rm -ti -v "${PWD}:/var/www/html/shop:cached" -p 8080:80 oxidesales/oxideshop-docker-php:7.4 composer create-project oxid-esales/oxideshop-project your_project_name dev-b-6.3-ce`

`cd Oxid-Verzeichnis`

`docker run --rm -ti -v "${PWD}:/var/www/html/shop:cached" -p 8080:80 oxidesales/oxideshop-docker-php:7.4 bash`

`apache2ctl start`

Now you can browse to http://localhost:8080/Setup

**Troubleshooting:**

_DB not reachable on Oxid-Setup:_

Find out the ip address of the container:

`docker inspect oxid_coding_days_mysql`

use the IP instead of the container name

**MySQL-DB:** 

`docker run --rm -ti --name oxid_coding_days_mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password -d mysql:5.7`

Now you can locally connect to the database using host “localhost” and Port 3306 (root:password)
