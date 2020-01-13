FROM docker.elastic.co/beats/filebeat:7.5.1

USER root

COPY filebeat.yml /usr/share/filebeat/filebeat.yml
COPY docker-entrypoint.sh /
RUN export PATH=$PATH:/usr/share/filebeat

RUN chown root:filebeat /usr/share/filebeat/filebeat.yml
RUN chmod +x /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh -e"]

USER filebeat

