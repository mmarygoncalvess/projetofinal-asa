FROM php:8.2-apache

# Instalar extensões PHP necessárias
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    libzip-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd zip pdo pdo_mysql

# Configurar o Apache
RUN a2enmod rewrite

# Baixar e instalar o WordPress
RUN curl -O https://wordpress.org/latest.tar.gz && \
    tar xzvf latest.tar.gz && \
    cp -R wordpress/* /var/www/html/ && \
    chown -R www-data:www-data /var/www/html

# Remover arquivos desnecessários
RUN rm -rf /var/www/html/index.html

# Copiar o arquivo de configuração do WordPress
COPY wp-config.php /var/www/html/wp-config.php

# Expor a porta 80
EXPOSE 80

# Iniciar o Apache
CMD ["apache2-foreground"]
