FROM mysql:8.0

# Copiar arquivo de configuração opcional do MySQL
COPY my.cnf /etc/mysql/my.cnf

# Definir variáveis de ambiente para o MySQL
ENV MYSQL_ROOT_PASSWORD=rootpassword
ENV MYSQL_DATABASE=wordpress
ENV MYSQL_USER=user
ENV MYSQL_PASSWORD=password

# Expor a porta padrão do MySQL
EXPOSE 3306

CMD ["mysqld"]
