# Proyecto Preta Ecommerce

Este proyecto configura un ecommerce utilizando un frontend en Vue.js con Vite y un backend en Laravel con PHP 8.2, todo desplegado usando Docker.

## Requisitos

- Docker
- Docker Compose

## Instalación y Configuración

### 1. Instalar Composer

Para instalar Composer, sigue estos pasos:

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
HASH=`curl -s https://composer.github.io/installer.sig`
php -r "if (hash_file('sha384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
sudo mv composer.phar /usr/local/bin/composer
composer --version
