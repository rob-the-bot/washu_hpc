FROM nvidia/cuda:12.4.1-cudnn-devel-ubuntu22.04
ENV DEBIAN_FRONTEND noninteractive

# Basic
RUN apt update
RUN apt -y upgrade
RUN apt -y install build-essential wget git cmake vim tmux nano rsync zip

# OpenCV
RUN apt -y install libopencv-dev

# General dependencies
RUN apt -y install libssl-dev libatlas-base-dev libprotobuf-dev libleveldb-dev libsnappy-dev libhdf5-serial-dev protobuf-compiler
RUN apt -y install --no-install-recommends libboost-all-dev

# Remaining dependencies, 14.04
RUN apt -y install libgflags-dev libgoogle-glog-dev liblmdb-dev

# OpenCL Generic
RUN apt -y install opencl-headers ocl-icd-opencl-dev
RUN apt -y install libviennacl-dev

# Clone Openpose and apply CUDNN8 fix
RUN git clone https://github.com/CMU-Perceptual-Computing-Lab/openpose /opt/openpose
WORKDIR /opt/openpose
RUN git fetch origin pull/2184/head:cudnn_fix
RUN git switch cudnn_fix

# Build Openpose
RUN mkdir /opt/openpose/build
WORKDIR /opt/openpose/build
RUN cmake \
    -D DOWNLOAD_BODY_25_MODEL=OFF \
    -D BUILD_PYTHON=OFF \
    -D USE_CUDNN=ON \
    -D CMAKE_BUILD_TYPE=Release \
    -D DOWNLOAD_HAND_MODEL=OFF \
    -D DOWNLOAD_FACE_MODEL=OFF \
	..

RUN make -j $(nproc) && make install
