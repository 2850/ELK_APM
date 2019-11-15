ARG ELK_VERSION

# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu

COPY plugin/elasticsearch-analysis-ik-7.4.1 /usr/share/elasticsearch/plugins/elasticsearch-analysis-ik-7.4.1
COPY plugin/elasticsearch-analysis-stconvert-7.4.1 /usr/share/elasticsearch/plugins/elasticsearch-analysis-stconvert-7.4.1
