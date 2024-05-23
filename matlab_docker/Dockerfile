FROM gcr.io/ris-registry-shared/matlab

RUN apt update
RUN apt install -y build-essential libgl1 libgl1-mesa-glx libxcursor1 libglib2.0-dev
RUN apt install -y htop vim nano tmux git rsync wget
RUN \
  wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh" && \
  bash Miniforge3-$(uname)-$(uname -m).sh -b -p /opt/conda && \
  rm Miniforge3-$(uname)-$(uname -m).sh
