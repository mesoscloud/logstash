FROM ubuntu:14.04

RUN apt-get update && \
apt-get install -y curl openjdk-7-jre-headless

RUN curl -fL https://download.elastic.co/logstash/logstash/logstash-1.5.4.tar.gz | tar xzf - -C /opt && \
mv /opt/logstash-1.5.4 /opt/logstash

ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/logstash/bin

CMD ["logstash"]
