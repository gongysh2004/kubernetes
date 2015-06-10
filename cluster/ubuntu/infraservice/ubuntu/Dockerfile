FROM ubuntu
MAINTAINER gong yong sheng  <gong.yongsheng@99cloud.net>

RUN apt-get update &&  apt-get -y -q install tcpdump dnsutils sysstat net-tools fio wget curl 

copy  pause /kubepause
ENTRYPOINT ["/kubepause"]
