FROM 		ubuntu:14.04
MAINTAINER 	Puja	

ADD https://dl.bintray.com/mitchellh/consul/0.5.2_linux_amd64.zip /tmp/consul.zip

RUN apt-get install -y unzip

RUN cd /usr/local/bin && unzip /tmp/consul.zip

RUN rm /tmp/consul.zip

ENTRYPOINT consul agent -server -data-dir /tmp/consul
