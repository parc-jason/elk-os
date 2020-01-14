FROM docker.elastic.co/beats/filebeat:7.5.1

USER root

COPY filebeat.yml /usr/share/filebeat/filebeat.yml

RUN export PATH=$PATH:/usr/share/filebeat && \
    chmod -R 0777 /usr/share/filebeat && \
    chmod go-w /usr/share/filebeat/filebeat.yml

