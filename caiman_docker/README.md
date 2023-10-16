# CaImAn Dockerfile

- Built based on [condaforge/mambaforge](https://hub.docker.com/r/condaforge/mambaforge), so `mamba` command is available
- Include common tools such as `gcc`, `rsync` and etc
- CaImAn environment is installed using `environment.yml` which is mostly taken from [here](https://github.com/flatironinstitute/CaImAn/blob/main/environment.yml), with some additional packages
- For now, CaImAn v1.9.16 is installed. It's from `pip` instead of `conda` because there were problems getting the environment to solve in `conda`
