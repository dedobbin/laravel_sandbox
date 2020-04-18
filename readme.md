## Requirements
- docker
- docker-compose
- PHP
- composer

#### Installing PHP7.3 (Ubuntu 18.04.3)
- apt-get update && apt-get upgrade
- apt-get install software-properties-common
- add-apt-repository ppa:ondrej/php
- apt-get update
- apt-get install php7.3
  
#### Composer (Ubuntu 18.04.3)
- apt-get install php7.3-dom
- apt-get install php7.3-mbstring
- php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
- php -r "if (hash_file('sha384', 'composer-setup.php') === 'a5c698ffe4b8e849a443b120cd5ba38043260d5c4023dbf93e1558871f1f07f58274fc6f4c93bcfd858c6bd0775cd8d1') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
- php composer-setup.php
- php -r "unlink('composer-setup.php');"
- mv composer.phar /usr/local/bin/composer

## Install
- composer install
- cp .env.example .env
- php artisan key:generate

## Start 
- docker-compose up
- localhost:8080
