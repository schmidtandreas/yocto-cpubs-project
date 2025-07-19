FROM ubuntu:24.04

RUN apt-get update && apt-get -y install \
    build-essential \
    bison \
    chrpath cpio \
    debianutils diffstat \
    file \
    flex \
    gawk gcc git \
    iputils-ping \
    libacl1 liblz4-tool locales \
    ncurses-dev \
    python3 python3-git python3-jinja2 python3-pexpect python3-pip python3-subunit \
    socat \
    sudo \
    texinfo \
    unzip \
    wget which \
    xz-utils \
    zstd
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

RUN rm /bin/sh && ln -s $(which bash) /bin/sh

RUN usermod -aG sudo ubuntu
RUN passwd -d ubuntu
RUN echo "ubuntu ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/ubuntu
RUN chmod 0440 /etc/sudoers.d/ubuntu

RUN locale-gen en_US.UTF-8 && update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

