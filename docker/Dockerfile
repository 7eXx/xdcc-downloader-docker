# start from basic debian
FROM debian:buster

ARG XDCC_DOWNLOADER_DEB=xdccdownloaderweb_1.3.7-1.deb

RUN apt-get update && \
    apt-get install -y \
    python \
    python-setuptools

WORKDIR /tmp

COPY docker/deb/${XDCC_DOWNLOADER_DEB} ${XDCC_DOWNLOADER_DEB}

RUN dpkg -i ${XDCC_DOWNLOADER_DEB}

COPY docker/start.sh start.sh

EXPOSE 8888

CMD ["sh", "./start.sh"]