FROM ubuntu
MAINTAINER Shun Wang

# Update sources
RUN echo "deb http://mirrors.sohu.com/ubuntu/ precise main restricted" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get upgrade -y

# Add lunchpad
RUN apt-get install -y python-software-properties
RUN add-apt-repository ppa:webupd8team/java -y
RUN apt-get update

# Install Oracle JDK 7
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN apt-get install -y --force-yes oracle-java7-installer -y
