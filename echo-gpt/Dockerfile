# syntax=docker.io/docker/dockerfile:1.4
FROM --platform=linux/riscv64 cartesi/python:3.10-slim-jammy
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    build-essential clang-15 \ 
    && rm -rf /var/apt/lists/*
    # lldb-15 lld-15 \
    # build-essential vim \

WORKDIR /opt/cartesi/dapp
COPY . .
RUN make
