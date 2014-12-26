FROM nownabe/ruby:2.2.0
MAINTAINER nownabe

RUN bundle install passenger --pre
RUN passenger-install-nginx-module --auto --languages ruby


