#Download the base image Ubuntu 16.04
FROM ubuntu:16.04

#Update Software repo
RUN apt-get update
RUN apt-get install -y curl openjdk-8-jre

RUN curl -L -O https://artifacts.elastic.co/downloads/logstash/logstash-5.1.2.tar.gz
RUN tar -xvf logstash-5.1.2.tar.gz -C /opt/

COPY logstash.conf /opt/logstash-5.1.2/config/logstash.conf

RUN rm  /logstash-5.1.2.tar.gz

RUN mkdir /opt/logstash-5.1.2/conf
CMD /opt/logstash-5.1.2/bin/logstash -f /opt/logstash-5.1.2/conf/logstash.conf

EXPOSE 5044
