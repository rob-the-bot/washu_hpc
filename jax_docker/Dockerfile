FROM d0ckaaa/ubuntu:gpu
ENV DEBIAN_FRONTEND noninteractive

RUN curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
RUN bash Miniforge3-$(uname)-$(uname -m).sh

RUN pip3 install -U "jax[cuda11_pip]" -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html
RUN pip3 install ipython jupyterlab ipywidgets seaborn
RUN pip3 install numpyro==0.12.1 -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html
