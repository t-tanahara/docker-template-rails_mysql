FROM ruby:2.5.1
RUN apt-get update -qq && apt-get install -y build-essential mysql-client nodejs

RUN mkdir /app
WORKDIR /app

ADD Gemfile /app/Gemfile
ADD Gemfile.lock /app/Gemfile.lock
RUN bundle install --without production
ADD . /app