FROM docker.elastic.co/beats/filebeat:7.5.1

USER root

COPY docker-entrypoint.sh /
COPY filebeat.yml /usr/share/filebeat/filebeat.yml

RUN export PATH=$PATH:/usr/share/filebeat && \
    chgrp -R 0 /usr/share/filebeat/filebeat && \
    chmod +x /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh", "-e"]

