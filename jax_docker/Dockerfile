FROM d0ckaaa/mamba

# download env config file
RUN wget https://raw.githubusercontent.com/rob-the-bot/washu_hpc/main/jax_docker/environment.yml
# create jax env
RUN mamba env create -f environment.yml
