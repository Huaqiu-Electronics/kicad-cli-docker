FROM debian:trixie



# install build dependencies
# --- MODIFICATION: Added 'locales' to the list ---
# --- MODIFICATION: Removed duplicate 'protobuf-compiler' at the end ---
RUN apt-get update && \
    apt-get install -y \
    locales \
    build-essential cmake libbz2-dev libcairo2-dev libglu1-mesa-dev \
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
    lld

# --- MODIFICATION START: Configure Locale to UTF-8 ---
# This ensures the dev container handles CJK filenames correctly
RUN sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
    locale-gen

ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8
# --- MODIFICATION END ---