FROM ubuntu:jammy

RUN apt-get update && apt-get install -y \
  build-essential \
  cmake \
  crossbuild-essential-amd64 \
  crossbuild-essential-arm64 \
  nano \
  ninja-build \
  pkg-config \
  python3 \
  python3-venv \
  subversion \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /root
ENV PATH="/root/venv/bin/:${PATH}"
RUN python3 -m venv venv && pip install conan && conan profile detect

