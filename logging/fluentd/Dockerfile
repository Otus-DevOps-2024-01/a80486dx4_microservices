# FROM fluent/fluentd:v1.10
FROM bitnami/fluentd:1.10.4

USER root
# RUN gem install fluent-plugin-elasticsearch --no-rdoc --no-ri --version 1.9.5
RUN gem install fluent-plugin-elasticsearch --version 1.9.5
# RUN gem install fluent-plugin-grok-parser --no-rdoc --no-ri --version 1.0.0
RUN gem install fluent-plugin-grok-parser --version 2.0.0

# FROM fluent/fluentd:v1.12.0-debian-1.0


# RUN gem uninstall -I elasticsearch && gem install elasticsearch -v 7.17.0  # replace broken elasticsearch library

# RUN gem install fluent-plugin-grok-parser --no-document --version 2.6.2
# RUN gem install fluent-plugin-elasticsearch --no-document --version 5.2.3

USER fluent

ADD fluent.conf /fluentd/etc
