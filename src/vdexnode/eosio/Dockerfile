FROM ubuntu:18.04

RUN apt-get update \
    && apt-get install -y wget \
    && wget https://github.com/eosio/eos/releases/download/v2.0.4/eosio_2.0.4-1-ubuntu-18.04_amd64.deb \
    && apt install -y ./eosio_2.0.4-1-ubuntu-18.04_amd64.deb \
    && rm ./eosio_2.0.4-1-ubuntu-18.04_amd64.deb \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /eosio \
    && mkdir /eosio/blocks \
    && mkdir -p /eosio/data \
    && mkdir -p /eosio/wallet

WORKDIR "/eosio"


EXPOSE 9876 8080 8888

COPY .  /eosio

RUN mv docker-entrypoint.sh /usr/local/bin/ \
    && chmod +x /usr/local/bin/docker-entrypoint.sh

ENTRYPOINT ["docker-entrypoint.sh"]
