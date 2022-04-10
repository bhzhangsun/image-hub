FROM ubuntu

COPY ./resource/ /tmp
RUN set -x && \
    export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get install -y tzdata ca-certificates && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai  /etc/localtime && \
    echo "/Asia/Shanghai" > /etc/timezone && \
    rm -rf /var/lib/apt/lists/* && \
    mv /etc/apt/sources.list /etc/apt/sources.list.bak && \
    mv /tmp/sources.list /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y wget git vim && \
    apt-get clean
