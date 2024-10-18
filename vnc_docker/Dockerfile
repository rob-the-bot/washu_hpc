FROM ghcr.io/washu-it-ris/novnc:ubuntu22.04
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install compilers and stuff for opencv
RUN apt install -y build-essential libgl1 libgl1-mesa-glx libxcursor1 libglib2.0-dev
# install useful packages
RUN apt install -y htop vim nano tmux git rsync wget
RUN apt install -y openssh-client aria2
# install conda
RUN wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh" && bash Miniforge3-$(uname)-$(uname -m).sh -b -p /opt/conda && rm Miniforge3-$(uname)-$(uname -m).sh
