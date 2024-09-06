FROM d0ckaaa/ubuntu
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

RUN apt update
# dependencies for IBAMR
RUN apt install -y mpich m4 python3-distutils libtirpc-dev cmake

# autoibamr to build IBAMR and other dependencies
RUN git clone https://github.com/ibamr/autoibamr.git /opt/autoibamr
WORKDIR /opt/autoibamr
RUN mkdir /opt/ibamr
RUN ./autoibamr.sh --ibamr-version 0.15.0 -p "/opt/ibamr" -j8 && chmod -R 777 /opt/ibamr

# build example
# WORKDIR /opt/ibamr/tmp/build/v0.15.0
# RUN make IB-ex0
