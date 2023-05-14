# syntax=docker.io/docker/dockerfile:1.4
FROM --platform=linux/riscv64 cartesi/python:3.10-slim-jammy
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    build-essential \
    && rm -rf /var/apt/lists/*

WORKDIR /opt/cartesi/dapp
COPY . .
RUN chown -R root /usr/include/riscv64-linux-gnu
# RUN cp /usr/include/riscv64-linux-gnu/stubs-lp64d.h /usr/include/riscv64-linux-gnu/stubs-lp64.h
RUN make
