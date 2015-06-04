FROM            ubuntu:14.04
MAINTAINER      Puja

ADD https://dl.bintray.com/mitchellh/consul/0.3.0_web_ui.zip /tmp/webconsul.zip

RUN apt-get install -y unzip
RUN mkdir /webconsul && cd /webconsul && unzip /tmp/webconsul.zip && rm /tmp/webconsul.zip && mv dist/* . && rm -rf dist

ADD https://dl.bintray.com/mitchellh/consul/0.5.2_linux_amd64.zip /tmp/consul.zip

RUN apt-get install -y unzip

RUN cd /usr/local/bin && unzip /tmp/consul.zip

RUN rm /tmp/consul.zip

EXPOSE 8500
