https://medium.com/@romaricp/the-perfect-kit-starter-for-a-symfony-4-project-with-docker-and-php-7-2-fda447b6bca1

**// Préparer Docker (vérifier les ports avant)**
docker-compose build
docker-compose up -d

**// Préparer Symfony**
docker exec -it -u dev pmk_php bash
cd /home/wwwroot/pmk
composer create-project symfony/skeleton my-temp-folder
cp -Rf /home/wwwroot/pmk/my-temp-folder/. .
rm -Rf /home/wwwroot/pmk/my-temp-folder

**// Donner les permissions** 
sudo chmod -R 777 var/cache
sudo chmod -R 777 var/log

**// User et passwords**
MYSQL_ROOT_PASSWORD: root
MYSQL_DATABASE: pmk
MYSQL_USER: pmk
MYSQL_PASSWORD: pmk



