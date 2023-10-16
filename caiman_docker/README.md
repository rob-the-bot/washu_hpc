# CaImAn Dockerfile

Available at [Docker Hub](https://hub.docker.com/repository/docker/d0ckaaa/caiman)

- Built based on [condaforge/mambaforge](https://hub.docker.com/r/condaforge/mambaforge), so `mamba` command is available
- Include common tools such as `gcc`, `rsync` and etc
- CaImAn is installed using `environment.yml` or `environment_win.yml`, both includes some additional packages. `environment_win.yml` is mostly taken from [here](https://github.com/flatironinstitute/CaImAn/blob/main/environment.yml). This separation is needed because currently [`tensorflow2` is removed in `conda-forge`](https://anaconda.org/conda-forge/tensorflow).
- For now, CaImAn v1.9.16 is installed
	+ Windows version is installed using `pip` instead of `conda`, due to the `tensorflow` problem mentioned above. So you might need to [Setting up environment variables](https://caiman.readthedocs.io/en/master/Installation.html#setting-up-environment-variables).
- Finall as always, remember to [Setting up caimanmanager](https://caiman.readthedocs.io/en/master/Installation.html#setting-up-caimanmanager) by yourself
