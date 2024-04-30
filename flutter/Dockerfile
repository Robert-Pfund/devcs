FROM ubuntu:20.04

RUN apt-get update -y && apt-get upgrade -y

RUN which which
RUN apt-get install -y curl git unzip xz-utils zip tar libglu1-mesa file wget gpg

RUN apt-get install -y cmake clang \
        ninja-build pkg-config \
        libgtk-3-dev liblzma-dev

RUN wget https://dl-ssl.google.com/linux/linux_signing_key.pub -O /tmp/google.pub
RUN gpg --no-default-keyring \
        --keyring /etc/apt/keyrings/google-chrome.gpg \
        --import /tmp/google.pub
RUN echo 'deb [arch=amd64 signed-by=/etc/apt/keyrings/google-chrome.gpg] http://dl.google.com/linux/chrome/deb/ stable main' | tee /etc/apt/sources.list.d/google-chrome.list
RUN apt-get update -y; apt-get install -y google-chrome-stable

RUN git clone -b master https://github.com/flutter/flutter.git
RUN /root/flutter/bin/flutter --version
