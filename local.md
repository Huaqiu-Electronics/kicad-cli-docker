# Setup Local dev

## install dependencies

apt-get update && \
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
 swig

## pull code

mkdir kicad-src
cd kicad-src

git clone git@gitlab.com:Liangtie/kicad.git;
git clone git@gitlab.com:kicad/libraries/kicad-symbols.git;
git clone git@gitlab.com:kicad/libraries/kicad-footprints.git;
git clone git@gitlab.com:kicad/libraries/kicad-templates.git;
git clone git@gitlab.com:kicad/libraries/kicad-packages3D.git

## build && install

export INSTALL_PREFIX=~/kicad-dev-bin
mkdir -p $INSTALL_PREFIX

cd kicad-src
pushd kicad

cmake \
 -G Ninja \
 -B build \
 -S . \
 -DKICAD_SCRIPTING_WXPYTHON=ON \
 -DKICAD_USE_OCC=ON \
 -DKICAD_SPICE=ON \
 -DKICAD_BUILD_I18N=ON \
 -DCMAKE_INSTALL_PREFIX=$INSTALL_PREFIX \
 -DKICAD_USE_CMAKE_FINDPROTOBUF=ON

cmake --build build
cmake --install build --prefix=$INSTALL_PREFIX

popd

pushd kicad-symbols

cmake \
-G Ninja \
-B build \
-S . \
-DCMAKE_RULE_MESSAGES=OFF \
-DCMAKE_VERBOSE_MAKEFILE=OFF \
-DCMAKE_INSTALL_PREFIX=$INSTALL_PREFI

cmake --build build
cmake --install build --prefix=$INSTALL_PREFIX

popd

pushd kicad-footprints

cmake \
-G Ninja \
-B build \
-S . \
-DCMAKE_RULE_MESSAGES=OFF \
-DCMAKE_VERBOSE_MAKEFILE=OFF \
-DCMAKE_INSTALL_PREFIX=$INSTALL_PREFI

cmake --build build
cmake --install build --prefix=$INSTALL_PREFIX

popd

pushd kicad-templates

cmake \
 -G Ninja \
-B build \
-S . \
-DCMAKE_RULE_MESSAGES=OFF \
 -DCMAKE_VERBOSE_MAKEFILE=OFF \
 -DCMAKE_INSTALL_PREFIX=$INSTALL_PREFI

cmake --build build
cmake --install build --prefix=$INSTALL_PREFIX

popd

pushd kicad-packages3D

cmake \
 -G Ninja \
 -B build \
 -S . \
 -DCMAKE_RULE_MESSAGES=OFF \
 -DCMAKE_VERBOSE_MAKEFILE=OFF \
 -DCMAKE_INSTALL_PREFIX=$INSTALL_PREFI

cmake --build build
cmake --install build --prefix=$INSTALL_PREFIX

popd
