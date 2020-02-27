FROM ruby:2-slim
LABEL version="1.0.0"

ENV BUNDLER_VERSION 2.0.2
RUN apt-get update && \
  apt-get install --no-install-recommends -y \
  && gem install bundler:2.0.2 \
  && bundle config --global silence_root_warning 1

COPY test.sh /

ENTRYPOINT ["sh", "/test.sh"]