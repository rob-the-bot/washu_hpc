FROM nvidia/cuda:11.6.2-cudnn8-runtime-ubuntu20.04
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install compilers and stuff for opencv
RUN apt install -y build-essential libgl1 libgl1-mesa-glx libxcursor1 libglib2.0-dev
RUN apt install -y htop vim nano tmux git rsync wget
# https://github.com/DeepLabCut/DeepLabCut/issues/2167
RUN apt install libc6
