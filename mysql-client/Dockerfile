FROM ubuntu:20.04
MAINTAINER Lingex <lingex@outlook.com>
LABEL Description="Image for maintenance MYSQL db"
WORKDIR /sql

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	mysql-client \
	nano \
	&& apt-get clean && rm -rf /var/lib/apt/lists/*
