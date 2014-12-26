FROM nownabe/ruby:2.2.0-jemalloc
MAINTAINER nownabe

RUN gem install passenger --prerelease
RUN passenger-install-nginx-module --auto --languages ruby


