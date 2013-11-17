FROM ubuntu
MAINTAINER Shun Wang

# Add mongodb sources
RUN echo "deb http://mirrors.sohu.com/ubuntu/ precise main restricted" > /etc/apt/sources.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv 7F0CEB10
RUN echo "deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen" > /etc/apt/sources.list.d/10gen.list
RUN apt-get update
RUN apt-get -y install apt-utils
RUN apt-get -y install mongodb-10gen

ADD mongodb.conf /etc/mongodb.conf
EXPOSE 27017

ENTRYPOINT ["/usr/bin/mongod", "--config", "/etc/mongodb.conf"]
