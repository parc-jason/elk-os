FROM docker.elastic.co/logstash/logstash:7.5.1

USER root

ENV XPACK_MONITORING_ELASTICSEARCH_HOSTS=elasticsearch
ENV ELASTICSEARCH_SERVICE_HOST=elasticsearch

RUN rm -f /usr/share/logstash/pipeline/logstash.conf
ADD pipeline/ /usr/share/logstash/pipeline/
RUN chmod -R g+r /usr/share/logstash/pipeline/

USER 1001
