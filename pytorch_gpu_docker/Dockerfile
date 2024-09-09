FROM pytorch/pytorch:2.4.0-cuda12.4-cudnn9-runtime
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install compilers and stuff for opencv
RUN apt install -y build-essential libgl1 libgl1-mesa-glx libxcursor1 libglib2.0-dev
# install some useful stuff
RUN apt install -y htop vim nano tmux git rsync wget

# install other packages
RUN conda install -n base -c conda-forge seaborn jupyterlab h5py scikit-learn -y
RUN pip install cebra
