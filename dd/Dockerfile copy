FROM php:7.2.1-cli-alpine3.7

ENV PAGEKIT_VERSION=1.0.13

# install dependencies via apk
RUN apk update && apk add  wget unzip zlib-dev

# install php-zip
RUN docker-php-ext-install -j$(nproc) zip


RUN mkdir /pagekit


COPY ./pagekit /pagekit

WORKDIR /pagekit

CMD ["php", "-S", "0.0.0.0:10000"]

EXPOSE  10000

