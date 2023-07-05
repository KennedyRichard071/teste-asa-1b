FROM ubuntu:latest

RUN apt-get update -y

RUN apt-get upgrade -y

RUN apt-get install postfix dovecot-imapd dovecot-pop3d telnet -y

COPY main.cf /etc/postfix

COPY start_email.sh /etc/init.d

RUN chmod 755 /etc/init.d/start_email.sh

EXPOSE 25/tcp 
EXPOSE 587/tcp  
EXPOSE 110/tcp
EXPOSE 143/tcp

CMD ["/etc/init.d/start_email.sh"]

#CMD ["/usr/sbin/postfix","start-fg"]