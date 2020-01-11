FROM docker.elastic.co/logstash/logstash:7.5.1

RUN rm -f /usr/share/logstash/pipeline/logstash.conf && \
  bin/logstash-plugin install logstash-input-udp

ADD pipeline/ /usr/share/logstash/pipeline/

EXPOSE 1025
