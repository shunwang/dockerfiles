FROM ubuntu
MAINTAINER Shun Wang

# Update sources
RUN echo "deb http://mirrors.sohu.com/ubuntu/ precise main restricted" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get upgrade -y

# Install Node.js
RUN apt-get -y install wget
RUN wget -O - http://nodejs.org/dist/v0.11.8/node-v0.11.8-linux-x64.tar.gz | tar -C /usr/local/ --strip-components=1 -zxv
