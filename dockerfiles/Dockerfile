FROM ghcr.io/taffish-org/minimap2:2.29

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN cd / && \
    git clone https://github.com/BGI-Qingdao/TGS-GapCloser.git && \
    cd /TGS-GapCloser/ && \
    rmdir /TGS-GapCloser/minimap2 && \
    ln -s /minimap2-2.29 /TGS-GapCloser/minimap2 && \
    make

ENV PATH=/TGS-GapCloser:{$PATH}

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=tgsgapcloser
