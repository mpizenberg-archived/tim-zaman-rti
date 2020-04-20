# cd src
# docker build -t tim-zaman-rti .
# cd ..
# docker run --rm -it --env="DISPLAY" -v /tmp/.X11-unix:/tmp/.X11-unix --device /dev/dri:/dev/dri --volume $(pwd):/rti tim-zaman-rti:latest

# Use bare ubuntu 16.04 (xenial)
FROM ubuntu:xenial

# Set working directory /rti
WORKDIR /rti

# Install dependencies
RUN apt update && apt upgrade -y && DEBIAN_FRONTEND=noninteractive apt install -y \
  build-essential \
  cmake \
  pkg-config \
  libboost-all-dev \
  libtbb-dev \
  qt5-default \
  libopencv-dev \
  ocl-icd-opencl-dev \
  beignet-opencl-icd \
  clinfo \
  liblcms2-dev \
  libconfig++-dev \
  libgphoto2-dev \
  libraw-dev \
  libexiv2-dev
