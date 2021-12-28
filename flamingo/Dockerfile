FROM ubuntu:20.04
MAINTAINER Lingex <lingex@outlook.com>
LABEL Description="For build & run flamingo: https://github.com/balloonwj/flamingo"
WORKDIR /work

ADD . /work

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	libmysqlclient-dev \
	gcc \
	g++ \
	cmake \
	&& apt-get clean && rm -rf /var/lib/apt/lists/*

ENV LANG C.UTF-8
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
