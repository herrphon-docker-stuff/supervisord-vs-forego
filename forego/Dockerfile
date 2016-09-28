FROM ubuntu:latest

RUN apt-get update \
 && apt-get install -y  \
           openssh-server  

ADD https://github.com/jwilder/forego/releases/download/v0.16.1/forego /usr/local/bin/forego
RUN chmod u+x /usr/local/bin/forego
RUN mkdir /var/run/sshd

COPY src/Procfile /root/
WORKDIR /root/

CMD ["forego", "start", "-r"]

