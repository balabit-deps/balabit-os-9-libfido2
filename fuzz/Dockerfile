# Copyright (c) 2019-2021 Yubico AB. All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM ubuntu:focal
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN apt-get install -y clang-12 cmake git libssl-dev libudev-dev make pkg-config
RUN apt-get install -y zlib1g-dev
RUN git clone --branch v0.9.0 https://github.com/PJK/libcbor
RUN git clone https://github.com/yubico/libfido2
RUN CC=clang-12 CXX=clang++-12 /libfido2/fuzz/build-coverage /libcbor /libfido2
