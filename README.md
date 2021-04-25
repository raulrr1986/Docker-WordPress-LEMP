# Requirements
Docker WordPress LEMP requires Docker version 1.12+ and Docker Compose.

# Installation
Download or Clone Docker WordPress LEMP. Once in the repository, run `docker-compose up` and you're up and running.

# Let's Start
WordPress on PHP7.4 + MySQL 8.0 with Docker Compose
Install WordPress on the latest LEMP stack using Docker Compose.

The following Docker images have been used:

PHP 7.4+
MariaDB
Latest WordPress version
Latest Nginx version stable
Installation (manual)
Clone repository:

git clone https://github.com/aurkenb/docker-wordpress-lemp && cd docker-wordpress-lemp
cp .env.example .env
Copy environment file and default nginx setup:

cp ./config/nginx/templates/http.conf ./config/nginx/default.conf
Adjust DOMAIN_NAME and other variables in .env:

DOMAIN_NAME=localhost.example

NGINX_HTTP_PORT=80
NGINX_HTTPS_PORT=443
...
Map DOMAIN_NAME to 127.0.0.1

echo "127.0.0.1 localhost.example" | sudo tee -a /etc/hosts
Ready to go:

docker-compose up -d --build
