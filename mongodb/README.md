# Simple MongoDB Dockerfile example

This Dockerfile allows you to build a Docker container with mongoDB in a
pretty 'default' state. 

The only added option is 'smallfiles' to make sure mongoDB doesn't claim 3Gb 
of space right away, but only about 512Mb.

Feel free to clone and use this as a template. Improvements are welcome.


## Build
* docker build -t shunwang/mongodb .

## Run
* docker run -d shunwang/mongodb

or have it mount a data dir on your host directory for your files.

* docker run -d -v /your/data/dir:/var/lib/mongodb shunwang/mongodb
