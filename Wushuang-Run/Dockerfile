FROM ubuntu:20.04
MAINTAINER Lingex <lingex@outlook.com>
LABEL Description="Image for running ws server"
WORKDIR /work

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	libxml2-utils \
	libboost-regex1.71.0 \
	liblog4cxx10v5 \
	libmysqlclient21 \
	&& apt-get clean && rm -rf /var/lib/apt/lists/*

ENV LANG C.UTF-8
