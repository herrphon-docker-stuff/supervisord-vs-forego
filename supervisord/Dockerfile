FROM ubuntu:latest

RUN apt-get update \
 && apt-get install -y  \
           openssh-server  \
           supervisor

COPY src/supervisord.conf /etc/supervisor/conf.d/supervisord.conf

CMD ["/usr/bin/supervisord"]

