FROM ruby

RUN apt-get update -y && apt-get install -y build-essential libpq-dev nodejs sqlite3


RUN gem install bundler -v 1.16.2 --no-document
RUN gem install rails --no-document
RUN gem install rake -v 12.3.1 --no-document

ONBUILD COPY  app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

#build from ft-rails folder :
#docker build -t ft-rails:on-build .

# ONBUILD  -  will run right after the FROM

# https://hub.docker.com/_/ruby
# https://guides.rubyonrails.org/getting_started.html