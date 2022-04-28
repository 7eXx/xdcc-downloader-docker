# start from basic debian
FROM debian:buster

ARG XDCC_DOWNLOADER_DEB=xdccdownloaderweb_1.3.7-1.deb

RUN apt-get update && \
    apt-get install -y \
    python \
    python-setuptools \
    net-tools \
    procps

WORKDIR /tmp

COPY docker/deb/${XDCC_DOWNLOADER_DEB} ${XDCC_DOWNLOADER_DEB}

RUN dpkg -i ${XDCC_DOWNLOADER_DEB}

COPY docker/entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

EXPOSE 8888

CMD [ "/entrypoint.sh" ]