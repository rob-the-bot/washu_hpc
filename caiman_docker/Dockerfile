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
RUN conda install mamba -n base -c conda-forge
RUN mamba create -n caiman
# install packages
RUN mamba install -n caiman -c conda-forge caiman shapely cython cvxpy natsort seaborn ffmpeg-python python-igraph jupyterlab jupyterlab-git jupyter_contrib_nbextensions nd2reader chart-studio plotly pytables openpyxl jupyterlab_code_formatter black isort pynrrd lmfit av numba llvmlite autograd oasis-deconv nibabel webcolors scikit-spatial emcee -y

# Make RUN commands use the new environment:
SHELL ["conda", "run", "-n", "caiman", "/bin/bash", "-c"]
RUN pip install antspyx nd2
