FROM ubuntu:latest

# Instalar Postfix
RUN apt-get update && apt-get install -y postfix

# Copiar arquivo de configuração
COPY main.cf /etc/postfix/main.cf

# Iniciar o serviço Postfix
CMD ["sh", "-c", "service postfix start && tail -f /var/log/mail.log"]
