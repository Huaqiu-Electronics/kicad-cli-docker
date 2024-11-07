FROM debian:bookworm

RUN sh -c 'echo "deb http://ftp.de.debian.org/debian sid main" >> /etc/apt/sources.list'
# install build dependencies
RUN apt-get update && \
    apt-get install -y build-essential cmake libbz2-dev libcairo2-dev libglu1-mesa-dev \
    libgl1-mesa-dev libglew-dev libx11-dev libwxgtk3.2-dev \
    mesa-common-dev pkg-config python3-dev python3-wxgtk4.0 \
    libboost-all-dev libglm-dev libcurl4-openssl-dev \
    libgtk-3-dev \
    libngspice0-dev \
    ngspice-dev \
    libocct-modeling-algorithms-dev \
    libocct-modeling-data-dev \
    libocct-data-exchange-dev \
    libocct-visualization-dev \
    libocct-foundation-dev \
    libocct-ocaf-dev \
    unixodbc-dev \
    zlib1g-dev \
    shared-mime-info \
    git \
    gettext \
    ninja-build \
    libgit2-dev \
    libsecret-1-dev \
    libnng-dev \
    protobuf-compiler \
    swig4.0 \
    python3-pip \
    python3-venv \
    libprotobuf-dev \
    protobuf-compiler \
    lld