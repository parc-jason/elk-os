FROM docker.elastic.co/beats/filebeat:7.5.1

USER root

COPY filebeat.yml /usr/share/filebeat/filebeat.yml
RUN export PATH=$PATH:/usr/share/filebeat

RUN chown root:filebeat /usr/share/filebeat/filebeat.yml

USER filebeat
CMD["exec", "filebeat", "-e"]

