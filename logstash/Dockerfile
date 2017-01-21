FROM ubuntu:14.04

RUN apt-get -yqq update
RUN apt-get -yqq install curl
RUN curl http://packages.elasticsearch.org/GPG-KEY-elasticsearch | apt-key add -

RUN echo 'deb http://packages.elasticsearch.org/logstash/1.4/debian stable main' > /etc/apt/sources.list.d/logstash.list
RUN apt-get -yqq update
RUN apt-get install -y logstash

ADD logstash.conf /etc/

WORKDIR /opt/logstash
ENTRYPOINT [ "bin/logstash" ]
CMD [ "--config=/etc/logstash.conf" ]
