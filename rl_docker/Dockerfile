FROM d0ckaaa/mamba

# download env config file
RUN wget https://raw.githubusercontent.com/rob-the-bot/washu_hpc/main/rl_docker/environment_cuda.yml -O env.yml
# create rl env
RUN mamba env create -f env.yml
