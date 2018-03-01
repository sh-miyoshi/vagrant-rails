FROM ruby:2.4.2
ENV LANG C.UTF-8
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs sqlite3
RUN gem install rails
RUN mkdir -p /myapp
EXPOSE 3000
COPY rails_server.sh /