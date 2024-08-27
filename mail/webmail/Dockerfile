FROM roundcube/roundcubemail:latest

# Copiar o arquivo de configuração do Roundcube
COPY config.inc.php /var/www/html/config/config.inc.php

# Expor a porta 80
EXPOSE 80

# Start Roundcube
CMD ["apache2-foreground"]
