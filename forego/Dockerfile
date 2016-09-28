FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update  \
 && apt-get -y upgrade  \
 && apt-get install psmisc  \
 && rm -rf /var/lib/apt/lists/*


ADD https://github.com/jwilder/forego/releases/download/v0.16.1/forego /usr/local/bin/forego
RUN chmod u+x /usr/local/bin/forego  \
 && mkdir /var/run/sshd

COPY     src/Procfile /root/
WORKDIR  /root/

CMD  ["forego", "start", "-r"]

