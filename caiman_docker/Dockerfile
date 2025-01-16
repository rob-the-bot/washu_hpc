FROM d0ckaaa/ubuntu
# create caiman env
RUN mamba env create --file=https://raw.githubusercontent.com/rob-the-bot/washu_hpc/main/caiman_docker/environment.yml
# fix for pynwb writing temp file
RUN chmod -R 777 /opt/conda/envs/caiman/lib/python3.10/site-packages/pynwb

