ARG ELK_VERSION

# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

USER root

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json

RUN yum update -y && yum install rsyslog -y
# ADD ./logentries.conf /etc/rsyslog.d/logentries.conf

RUN logstash-plugin install logstash-filter-jdbc_streaming
RUN logstash-plugin install logstash-filter-aggregate
RUN logstash-plugin install logstash-input-jdbc
RUN logstash-plugin install logstash-filter-translate

COPY driver/mssql-jdbc-7.4.1.jre11.jar /usr/share/logstash/logstash-core/lib/jars/mssql-jdbc-7.4.1.jre11.jar