
#Download the base image Ubuntu 16.04
FROM ubuntu:16.04

#Update Software repo
RUN apt-get update
RUN apt-get install -y curl openjdk-8-jre
RUN useradd euser -U
RUN curl -L -O https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-5.1.2.tar.gz
RUN tar -xvf elasticsearch-5.1.2.tar.gz -C /opt/
RUN chown -R euser  /opt/elasticsearch-5.1.2

COPY elasticsearch.yml /opt/elasticsearch-5.1.2/config
COPY logging.yml /opt/elasticsearch-5.1.2/config

RUN rm  /elasticsearch-5.1.2.tar.gz

CMD /opt/elasticsearch-5.1.2/bin/elasticsearch  

USER euser
EXPOSE 9200 9300

