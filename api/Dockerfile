FROM ruby:2.5.8
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client
RUN mkdir /api
WORKDIR /api
COPY Gemfile /api/Gemfile
COPY Gemfile.lock /api/Gemfile.lock
RUN gem install bundler && bundle install && rails db:migrate
COPY . /api
EXPOSE 3000
RUN rails server -p 3000 -b '0.0.0.0'