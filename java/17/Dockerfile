FROM        --platform=$TARGETOS/$TARGETARCH eclipse-temurin:17-jre-jammy

LABEL       author="Fukumaisaba"\
            maintainer="contact@fukumaisaba.net"\
            org.opencontainers.image.source="https://github.com/MCFukumaisaba/Docker-Images"\
            org.opencontainers.image.licenses=MIT

RUN 		useradd -d /home/container -m container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]