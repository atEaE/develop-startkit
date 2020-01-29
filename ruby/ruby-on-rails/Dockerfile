FROM ruby:2.6.5-alpine

# basic setting
ENV LANG C.UTF-8
RUN apk add --update-cache \
        mysql-client \
        mysql-dev \
        libxslt-dev \
        libxml2-dev \
        build-base \
        yarn \
        tzdata \
        git \
        bash \
        perl \
        file \
        imagemagick \
    --no-cache

# create workspace
WORKDIR /app
ADD . /app

# install package
RUN bundle install && yarn install
RUN rails webpacker:install