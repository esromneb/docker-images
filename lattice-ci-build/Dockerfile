# ARG VERILATOR_VERSION=2825940
ARG VERILATOR_VERSION=verilator_4_016
FROM ubuntu:18.04

ARG DEBIAN_FRONTEND=noninteractive


RUN apt-get update && apt-get install apt-utils -y
RUN apt-get upgrade -y
RUN apt-get update && apt-get install -y \
cmake make wget unzip tar build-essential python3 python3-pip git \
flex bison autoconf

# Checkout CIRCT and LLVM
RUN git clone https://github.com/verilator/verilator /tmp/verilator && \
cd /tmp/verilator && \
git checkout $VERILATOR_VERSION && \
git submodule update --init --depth 1

RUN cd /tmp/verilator && autoconf && ./configure && make -j2 && make install

