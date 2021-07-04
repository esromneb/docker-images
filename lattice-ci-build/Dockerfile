# ARG VERILATOR_VERSION=2825940
# ARG VERILATOR_VERSION=verilator_4_016
FROM ubuntu:18.04

ARG DEBIAN_FRONTEND=noninteractive


RUN apt-get update && apt-get install apt-utils -y
RUN apt-get update && apt-get install -y \
cmake make iproute2


RUN ip a
