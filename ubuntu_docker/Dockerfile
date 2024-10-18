FROM ubuntu:22.04
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install compilers and stuff for opencv
RUN apt install -y build-essential libgl1 libgl1-mesa-glx libxcursor1 libglib2.0-dev
RUN apt install -y htop vim nano tmux git rsync wget

# install package which makes downloading (from collaborators) faster
RUN apt install -y aria2

# install 7z
RUN apt install -y p7zip-full p7zip-rar
