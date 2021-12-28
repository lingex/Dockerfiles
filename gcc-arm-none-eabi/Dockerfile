FROM alpine:latest
MAINTAINER Lingex <lingex@outlook.com>
LABEL Description="Image for building arm-embedded projects"
WORKDIR /work

ADD . /work

RUN apk update && apk add --no-cache make newlib-arm-none-eabi gcc g++ gcc-arm-none-eabi
