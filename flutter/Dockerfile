FROM dart:3.3.1-sdk

RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install -y curl git unzip xz-utils zip tar libglu1-mesa file which

RUN git clone -b master https://github.com/flutter/flutter.git
RUN /root/flutter/bin/flutter --version
