FROM antsx/ants:master
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# install useful packages
RUN apt install -y htop vim nano tmux git rsync wget curl

# install package which makes downloading (from collaborators) faster
RUN apt install -y aria2

# install 7z
RUN apt install -y p7zip-full
