git clone https://github.com/dimlen/oxid-php-apache.git
cd oxid-php-apache
./build.sh 7.4
cd Oxid-Verzeichnis
docker run --rm -ti -v "${PWD}:/var/www/html/shop:cached" -p 8080:80 oxidesales/oxideshop-docker-php:7.4 bash
composer create-project --no-dev oxid-esales/oxideshop-project your_project_name dev-b-6.3-ce

In der Bash "apache2ctl start"

MySQL-DB: docker run --rm -ti --name oxid_coding_days_mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password -d mysql:latest

Now you can connect to the database using host “localhost” and Port 3306 (root:password)
