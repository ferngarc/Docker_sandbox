FROM ruby:2.3-slim
MAINTAINER odnanref <fernn.garcc@gmail.com>

RUN apt-get update && apt-get install -qq -y build-essential nodejs libpq-dev postgresql-client-9.4 --fix-missing --no-install-recommends

ENV INSTALL_PATH /stanley
RUN mkdir -p $INSTALL_PATH

WORKDIR $INSTALL_PATH

COPY Gemfile Gemfile
RUN bundle install

COPY . .
