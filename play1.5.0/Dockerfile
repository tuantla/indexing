FROM indexing/jvm
RUN apk add --no-cache curl python unzip
ENV PLAY_VERSION 1.5.0
ENV JAVA_HOME /opt/jdk

WORKDIR /opt/play
RUN curl -s -o play-${PLAY_VERSION}.zip  https://downloads.typesafe.com/play/${PLAY_VERSION}/play-${PLAY_VERSION}.zip && \
        unzip play-${PLAY_VERSION}.zip && rm play-${PLAY_VERSION}.zip && mv play-${PLAY_VERSION} play1

ENV PATH $PATH:$JAVA_HOME:/opt/play/play1
ENTRYPOINT ["play"]
WORKDIR /app/
EXPOSE 9000
