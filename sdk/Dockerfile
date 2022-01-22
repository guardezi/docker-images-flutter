FROM cirrusci/android-sdk:30
# FROM node:slim
USER root



ENV FLUTTER_HOME=${HOME}/sdks/flutter \
    FLUTTER_VERSION=stable
ENV FLUTTER_ROOT=$FLUTTER_HOME

ENV PATH ${PATH}:${FLUTTER_HOME}/bin:${FLUTTER_HOME}/bin/cache/dart-sdk/bin

RUN git clone --depth 1 --branch ${FLUTTER_VERSION} https://github.com/flutter/flutter.git ${FLUTTER_HOME}

RUN flutter precache

RUN yes | flutter doctor --android-licenses \
    && flutter doctor \
    && chown -R root:root ${FLUTTER_HOME}

RUN curl -O https://github.com/google/bundletool/releases/download/1.7.0/bundletool-all-1.7.0.jar
RUN mv bundletool-all-1.7.0.jar bundletool.jar

RUN apt-get update -qqy && apt-get install -qqy \
        curl \
        gcc \
        python3-dev \
        python3-pip \
        apt-transport-https \
        lsb-release \
        openssh-client \
        git \
        gnupg \
        openjdk-11-jdk \
        unzip
RUN pip3 install -U crcmod

RUN curl -sL https://firebase.tools | bash
RUN curl -O https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-340.0.0-linux-x86_64.tar.gz

RUN tar -xvf google-cloud-sdk-340.0.0-linux-x86_64.tar.gz -C /opt

RUN /opt/google-cloud-sdk/install.sh --quiet

ENV PATH ${PATH}:/opt/google-cloud-sdk/bin

#installing sonar scanner
RUN curl -O https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.6.2.2472.zip
RUN unzip sonar-scanner-cli-4.6.2.2472.zip -d /opt

ENV PATH ${PATH}:/opt/sonar-scanner-4.6.2.2472/bin

