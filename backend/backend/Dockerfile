# Usar la imagen oficial de PHP 8.2 con Apache
FROM php:8.2-apache

# Instalar extensiones necesarias de PHP
RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    libzip-dev \
    zip \
    unzip \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install pdo_mysql zip

# Habilitar el módulo de reescritura de Apache
RUN a2enmod rewrite

# Establecer el directorio de trabajo
WORKDIR /var/www/html

# Copiar el archivo de configuración de Apache
COPY ./apache/000-default.conf /etc/apache2/sites-available/000-default.conf

# Copiar los archivos del proyecto al contenedor
COPY . /var/www/html

# Instalar las dependencias de Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer install

# Dar permisos a las carpetas de Laravel
RUN chown -R www-data:www-data /var/www/html/storage /var/www/html/bootstrap/cache

# Exponer el puerto 80
EXPOSE 80

# Ejecutar Apache en primer plano
CMD ["apache2-foreground"]
