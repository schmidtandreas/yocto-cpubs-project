FROM ubuntu:24.04

RUN apt-get update && apt-get -y install \
    build-essential \
    chrpath cpio \
    debianutils diffstat \
    file \
    gawk gcc git \
    iputils-ping \
    libacl1 liblz4-tool locales \
    python3 python3-git python3-jinja2 python3-pexpect python3-pip python3-subunit \
    socat \
    texinfo \
    unzip \
    wget which \
    xz-utils \
    zstd
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

RUN rm /bin/sh && ln -s $(which bash) /bin/sh

RUN locale-gen en_US.UTF-8 && update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

