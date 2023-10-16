FROM d0ckaaa/ubuntu

ENV PATH="/opt/conda/bin:${PATH}"
ARG PATH="/opt/conda/bin:${PATH}"

# install miniconda
RUN wget \
    https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh \
    && bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda\
    && rm -f Miniconda3-latest-Linux-x86_64.sh 

RUN conda config --set always_yes yes
RUN conda update --yes conda

# create caiman env
# RUN conda install mamba -n base -c conda-forge
RUN conda create -n caiman
# install packages
RUN conda env create -f environment.yml -n caiman
# Make RUN commands use the new environment:
SHELL ["conda", "run", "-n", "caiman", "/bin/bash", "-c"]
