FROM nvidia/cuda:12.4.1-cudnn-runtime-ubuntu22.04
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install compilers and stuff for opencv
RUN apt install -y build-essential libgl1 libgl1-mesa-glx libxcursor1 libglib2.0-dev
# install useful packages
RUN apt install -y htop vim nano tmux git rsync wget
# https://github.com/DeepLabCut/DeepLabCut/issues/2167
RUN apt install libc6
