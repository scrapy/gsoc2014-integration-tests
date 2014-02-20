# mitmproxy dockerfile

FROM ubuntu

MAINTAINER Nitin Agarwal, nitinagarwal3006@gmail.com

RUN apt-get update

RUN apt-get install -y python-pip python-dev libevent1-dev libxml2-dev libxslt-dev
RUN apt-get install -y -q build-essential

RUN pip install --upgrade pip
RUN pip install mitmproxy


# Expose port
EXPOSE 8080		#default port

# mitmproxy need utf8
ENV LANG en_US.UTF-8


ENTRYPOINT ["mitmproxy"]


