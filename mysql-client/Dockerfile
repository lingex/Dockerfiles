FROM ubuntu:20.04
MAINTAINER Lingex <lingex@outlook.com>
LABEL Description="Image for running ws server"
WORKDIR /sql

ADD . /sql

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	mysql-client \
	nano \
	lrzsz \
	&& apt-get clean && rm -rf /var/lib/apt/lists/*

ENV LANG C.UTF-8
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
