FROM ruby:3.2.2
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    default-mysql-client \
    nodejs \
    sudo \
    vim

RUN mkdir /app
WORKDIR /app
COPY Gemfile /app/
# COPY Gemfile.lock /app/
RUN bundle install