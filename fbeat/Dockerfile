FROM docker.elastic.co/beats/filebeat:7.5.1

COPY filebeat.yml /usr/share/filebeat/filebeat.yml
USER root
RUN export PATH=$PATH:/usr/share/filebeat

RUN chown root:filebeat /usr/share/filebeat/filebeat.yml
USER filebeat

ENTRYPOINT ["/usr/local/bin/docker-entrypoint -e"]
