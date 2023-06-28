FROM ubuntu:latest

RUN apt-get update -y

RUN apt-get upgrade -y

RUN apt-get install postfix telnet -y

EXPOSE 25/tcp 
EXPOSE 587/tcp  

CMD ["/usr/sbin/postfix","start-fg"]