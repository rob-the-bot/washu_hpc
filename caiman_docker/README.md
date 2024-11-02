# CaImAn Dockerfile

Available at [Docker Hub](https://hub.docker.com/repository/docker/d0ckaaa/caiman)

- Built based on [d0ckaaa/ubuntu]([https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html#docker-images](https://hub.docker.com/repository/docker/d0ckaaa/ubuntu)).
Include common tools such as `gcc`, `rsync` and etc, `mamba` command is available for solving dependencies faster.
- CaImAn is installed using `environment.yml`, both include some additional packages.
Windows user might need to install tensorflow from the `anaconda` channel separately first, since `conda-forge` channel doesn't provide the latest tensorflow.
For now, CaImAn v1.11.3 is installed
- Finally as always, remember to [Setting up caimanmanager](https://caiman.readthedocs.io/en/master/Installation.html#setting-up-caimanmanager) by yourself
