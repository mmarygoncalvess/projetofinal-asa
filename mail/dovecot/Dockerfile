FROM dovecot/dovecot

COPY dovecot.conf /etc/dovecot/dovecot.conf
RUN service dovecot start

# Criar usuários genéricos
RUN useradd -m user1 -s /bin/bash && echo "user1:password1" | chpasswd
RUN useradd -m user2 -s /bin/bash && echo "user2:password2" | chpasswd
