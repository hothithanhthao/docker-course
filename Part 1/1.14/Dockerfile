FROM ruby:2.6.0
COPY rails-example-project-master /Users/Risa/Desktop/www/ruby
WORKDIR /Users/Risa/Desktop/www/ruby

RUN apt-get update && apt-get install -y nodejs 
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash - && apt-get update && apt-get install -y nodejs

RUN gem install bundler
RUN bundle install

RUN rails db:migrate && rake assets:precompile


EXPOSE 3000
CMD ["rails", "s"]