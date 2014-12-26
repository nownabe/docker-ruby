FROM nownabe/ruby:latest-passenger-pre
MAINTAINER nownabe

COPY nginx.conf /opt/nginx/conf/nginx.conf

RUN bundle config --global frozen 1

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY Gemfile /usr/src/app/
ONBUILD COPY Gemfile.lock /usr/src/app/
ONBUILD RUN bundle install

ONBUILD COPY . /usr/src/app

CMD ["/opt/nginx/sbin/nginx", "-c", "/opt/nginx/conf/nginx.conf"]

EXPOSE 80
