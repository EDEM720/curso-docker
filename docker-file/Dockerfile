FROM ubuntu:22.04
ARG DATE
ARG VERSION=1.18.*
ENV DATABASE_IP="192.168.2.1"
ENV DATABASE_PORT=5432
RUN apt-get update
RUN apt-get -y install nginx=$VERSION
RUN apt-get -y install tree
ADD html/ /var/www/html
EXPOSE 80
ENTRYPOINT [ "/usr/sbin/nginx" ]
CMD [ "-g", "daemon off;" ]
MAINTAINER Evio Estelin <danel720@hotmail.com>
WORKDIR /var/tmp
LABEL base.version="$VERSION"
LABEL base.build.date="$DATE"
