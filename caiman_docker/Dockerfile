FROM condaforge/mambaforge

# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install compilers and stuff for opencv
RUN apt install -y build-essential libgl1 libgl1-mesa-glx libxcursor1 libglib2.0-dev
RUN apt install -y htop vim nano tmux git rsync wget

# install packages which makes downloading (from collaborators) faster
RUN apt install -y aria2

# conda stuff
RUN conda config --set always_yes yes
# create caiman env
RUN conda remove -n caiman --all
# install packages
RUN wget https://raw.githubusercontent.com/rob-the-bot/washu_hpc/main/caiman_docker/environment.yml
RUN mamba env create -f environment.yml
# Make RUN commands use the new environment:
SHELL ["conda", "run", "-n", "caiman", "/bin/bash", "-c"]
