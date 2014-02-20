# vaurien dockerfile

FROM ubuntu

MAINTAINER Nitin Agarwal, nitinagarwal3006@gmail.com

RUN apt-get update

RUN apt-get install -y python-pip python-dev libevent1-dev libxml2-dev libxslt-dev
RUN apt-get install -y -q build-essential

RUN pip install --upgrade pip
RUN pip install vaurien


# Expose port
EXPOSE 8080		#default port


ENTRYPOINT ["vaurien"]

