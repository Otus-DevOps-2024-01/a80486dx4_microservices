FROM fluent/fluentd:v0.12-debian

RUN gem install fluent-plugin-elasticsearch --no-rdoc --no-ri --version 1.17.2
RUN gem install fluent-plugin-grok-parser --no-rdoc --no-ri --version 1.0.0
ADD fluent.conf /fluentd/etc
