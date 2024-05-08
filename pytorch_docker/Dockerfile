FROM pytorch/pytorch:2.3.0-cuda11.8-cudnn8-runtime
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install some useful stuff
RUN apt install -y htop vim nano tmux git rsync wget

RUN wget https://raw.githubusercontent.com/licksylick/AutoTrackAnything/main/requirements.txt
RUN pip3 install -r requirements.txt
