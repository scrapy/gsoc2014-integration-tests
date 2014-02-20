# web-polygraph dockerfile

FROM ubuntu

MAINTAINER Nitin Agarwal, nitinagarwal3006@gmail.com

RUN apt-get update
RUN apt-get install -y wget


Run wget http://www.web-polygraph.org/downloads/srcs/polygraph-4.3.2-src.tgz
RUN tar xvzf polygraph-4.3.2-src.tgz | rm polygraph-4.3.2-src.tgz
RUN cd polygraph-4.3.* | ./configure


RUN apt-get install -y -q build-essential
RUN apt-get install -y -q g++


# Expose port
EXPOSE 8999		# this is not the default port


ENTRYPOINT ["polygraph"]

