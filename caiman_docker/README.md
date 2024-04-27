# CaImAn Dockerfile

Available at [Docker Hub](https://hub.docker.com/repository/docker/d0ckaaa/caiman)

- Built based on [miniforge](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html#docker-images), so `mamba` command is available for solving dependencies faster
- Include common tools such as `gcc`, `rsync` and etc
- CaImAn is installed using `environment.yml`, both include some additional packages. Windows user might need to install tensorflow from the `anaconda` channel separately first, since `conda-forge` channel doesn't provide the latest tensorflow
- For now, CaImAn v1.10.4 is installed
- Finally as always, remember to [Setting up caimanmanager](https://caiman.readthedocs.io/en/master/Installation.html#setting-up-caimanmanager) by yourself
