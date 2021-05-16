FROM cirrusci/android-sdk:30
# FROM node:slim
USER root

RUN curl -sL https://firebase.tools | bash


ENV FLUTTER_HOME=${HOME}/sdks/flutter \
    FLUTTER_VERSION=stable
ENV FLUTTER_ROOT=$FLUTTER_HOME

ENV PATH ${PATH}:${FLUTTER_HOME}/bin:${FLUTTER_HOME}/bin/cache/dart-sdk/bin

RUN git clone --depth 1 --branch ${FLUTTER_VERSION} https://github.com/flutter/flutter.git ${FLUTTER_HOME}

RUN yes | flutter doctor --android-licenses \
    && flutter doctor \
    && chown -R root:root ${FLUTTER_HOME}
