FROM d0ckaaa/ubuntu
# Choosing the noninteractive mode to avoid all the input during docker image build
ENV DEBIAN_FRONTEND noninteractive

# dependencies for IBAMR
RUN apt install -y mpich m4 python3-distutils libtirpc-dev

# autoibamr to build IBAMR and other dependencies
RUN git clone https://github.com/ibamr/autoibamr.git /opt/autoibamr
WORKDIR /opt/autoibamr
RUN mkdir /opt/ibamr
RUN ./autoibamr.sh -p "/opt/ibamr" -j8 && chmod -R 777 /opt/ibamr

# build example
# WORKDIR /opt/ibamr/tmp/build/v0.12.1
# RUN make IB-ex0
