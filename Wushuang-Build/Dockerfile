FROM ubuntu:20.04
MAINTAINER Lingex <lingex@outlook.com>
LABEL Description="Image for build and run ws projects"
WORKDIR /work

#ADD ./work

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
        libmysqlclient-dev \
        #build-essential \
        openssh-server \
        git \
        nano \
        libboost-regex-dev \
        liblog4cxx-dev* \
        libxml2-dev \
        gcc \
        g++ \
        cmake \
        gdb \
        ccache \
        && apt-get clean && rm -rf /var/lib/apt/lists/*


# nano show constant
RUN sed -i 's/# set constantshow/ set constantshow/g' /etc/nanorc

# workdir for ssh
RUN mkdir -p /run/sshd

# allow root to login
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config

# allow public key login
RUN sed -i 's/#PubkeyAuthentication yes/PubkeyAuthentication yes/g' /etc/ssh/sshd_config

ENV LANG C.UTF-8
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

EXPOSE 22 21000 21118

ENTRYPOINT ["/usr/sbin/sshd", "-D", "-o", "ListenAddress=0.0.0.0"]

