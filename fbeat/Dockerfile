FROM docker.elastic.co/beats/filebeat:7.5.1

COPY filebeat.yml /usr/share/filebeat/filebeat.yml
USER root
RUN chown root:filebeat /usr/share/filebeat/filebeat.yml
USER filebeat

ENTRYPOINT ["bash","-c","export PATH=$PATH:/usr/share/filebeat && /usr/local/bin/docker-entrypoint -e"]
