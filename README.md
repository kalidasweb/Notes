SFA Installation
===================================
## Stack: 
     LEMP
## Requirements:
* PHP 7.0^
* PHP extensions (bcmath,mbstring,xml,zip,gd,mysql,redis,curl)
* Composer
* Git (Version Control)
* NodeJS 
* NPM 
* Redis Database
* MariaDB / MySql Database
* uWebSockets (to improve the web socket performance)
* Laravel Mix
* Laravel Echo Server (For WebSocket)
* Nginx
## Env Config: 

### Update Machine:
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install software-properties-common
```
### Install PHP: 
```bash
      sudo apt-get install php-fpm 
```

### Install PHP Ext:
```bash
sudo apt-get install  php-bcmath  php-mbstring  php-xml php-zip  php-gd  php-mysql php-redis  php-curl
```  
### Install Composer:
```bash
sudo apt-get install curl
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```
### Install Git:
```bash
sudo apt-get install git  
```   
### Install NodeJS:
```bash
sudo apt-get install nodejs 
```
### Install NPM:
```bash
sudo apt-get install npm 
```
### Install Redis:
```bash
sudo apt-get install redis-server
```
### Install MariaDB:
```bash
sudo apt-get install mariadb-server
```
During installation it will ask you for the root user password 
### Install uWebSockets:
https://github.com/uNetworking/uWebSockets
### Install laravel-echo-server:
```bash
sudo npm -g install laravel-echo-server
```

## Clone the Code base:
```bash
git clone https://kalidass_web@bitbucket.org/kalidass_web/sfa.git codebase_foldername
```
## Create Mysql Database:
```bash
mysql -u root -p 
```
will ask for root user password (refer Install MariaDB)
```bash
create database sfa_database;
use sfa_database
export codebase_foldername/db-s/super_admin_db.sql 
```
## Config Codebase:
```bash
cd codebase_foldername/
composer install
cp env.example .env 
```
now .env file will be created change the paths of Sql,then Change the database credentials in file config/database.php or add the database credentials in .env

## Run Code:
Terminal Tab1:
```bash
 laravel-echo-server start
 ```
Terminal Tab2:
```bash
 php artisan serve
 ```

## now our ship ready

# Documents:

https://laravel.com/docs/

https://www.w3schools.com/angular/

https://redis.io/commands

https://github.com/tlaverdure/laravel-echo-server

https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-16-

https://php-fpm.org/
