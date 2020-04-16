# Docker Startup
Docker LAMP container configured for a Symfony 3+ projects but it can be easily adjusted for any PHP based framework.

## Included software
- PHP 7.3.1
- MySQL (latest)
- Apache 2.4.25
- MailDev 1.0.0-rc3

## Installation
- Clone this into your project root directory
- To start new Symfony project run `composer create-project symfony/website-skeleton web` or `symfony new --full web`.
- If you use framework that does have `index.php` file in your project root, instead of `/public` or uses other structure: 
    - Create `/web/public` directory and place your framework into `/web/public` if your framework doesn't separate public code from framework.
    - Create `/web` directory and modify line `4` of `.docker/apache/vhosts/site.conf` to match your framework structure. 
- Run `docker-compose build`

## Usage
### How to start server
`docker-compose run`
### How to login into containers console
- Apache: `docker container exec -it apache_container bash`
- PHP: `docker container exec -it php_container bash`
- MySQL: `docker container exec -it mysql_container bash`
- PHPMyAdmin: `docker container exec -it phpmyadmin_container bash`
- MailDev: `docker container exec -it maildev_container bash`
### Server URL's
- Webserver (main) http://localhost
- PHPMyAdmin http://localhost:8080
- MailDev http://localhost:8081

