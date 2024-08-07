FROM        --platform=$TARGETOS/$TARGETARCH eclipse-temurin:17-jre-jammy

LABEL       author="Fukumaisaba"\
            maintainer="contact@fukumaisaba.net"\
            org.opencontainers.image.source="https://github.com/MCFukumaisaba/Docker-Images"\
            org.opencontainers.image.licenses=MIT

RUN         sed -i.bak -r 's@http://(jp\.)?archive\.ubuntu\.com/ubuntu/?@https://ftp.udx.icscoe.jp/Linux/ubuntu/@g' /etc/apt/sources.list\
            && apt update -y\
            && apt install -y iproute2\
            && useradd -d /home/container -m container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]