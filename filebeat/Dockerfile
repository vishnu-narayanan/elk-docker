#Download the base image Ubuntu 16.04
FROM ubuntu:16.04

#Update Software repo
RUN apt-get update

RUN apt-get install -y  wget
RUN wget https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-5.1.2-linux-x86_64.tar.gz

RUN tar -xzvf filebeat-5.1.2-linux-x86_64.tar.gz -C /opt/

#COPY filebeat.yml /opt/filebeat-5.1.2-linux-x86_64/config/filebeat.yml

RUN rm  /filebeat-5.1.2-linux-x86_64.tar.gz

RUN mkdir /opt/filebeat-5.1.2-linux-x86_64/conf

CMD /opt/filebeat-5.1.2-linux-x86_64/filebeat -e -c /opt/filebeat-5.1.2-linux-x86_64/conf/filebeat.yml

