FROM ruby:2.5.8
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client
RUN mkdir /api
WORKDIR /api
COPY Gemfile /api/Gemfile
COPY Gemfile.lock /api/Gemfile.lock
COPY Rakefile /api/Rakefile
RUN gem install bundler && bundle install && rake db:create && rake db:migrate
COPY . /api
EXPOSE 3000