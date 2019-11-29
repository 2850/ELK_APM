ARG ELK_VERSION

# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu

COPY plugin/analysis-ik-7.3.0 /usr/share/elasticsearch/plugins/analysis-ik-7.3.0
COPY plugin/analysis-stconvert-7.3.0 /usr/share/elasticsearch/plugins/analysis-stconvert-7.3.0
COPY plugin/jieba /usr/share/elasticsearch/plugins/jieba