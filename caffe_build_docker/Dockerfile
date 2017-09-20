# CURRENTLY UNTESTED

# Install Ubuntu 14.04 with CUDA 8
FROM kaixhin/cuda-caffe:8.0

# Install general dependencies for building caffe
RUN sudo apt-get update
RUN sudo apt-get -y install libprotobuf-dev libleveldb-dev libsnappy-dev libopencv-dev libhdf5-serial-dev protobuf-compiler
RUN sudo apt-get -y install --no-install-recommends libboost-all-dev

# Install BLAS
RUN sudo apt-get -y install libatlas-base-dev

# Install Pycaffe
RUN sudo apt-get -y install python-dev

# Remaining dependencies
RUN sudo apt-get install -y libgflags-dev libgoogle-glog-dev liblmdb-dev
RUN sudo apt-get install -y doxygen

# Clone caffe_lrcn
RUN sudo apt-get install -y git
RUN cd /root/ && git clone https://github.com/anguyen8/caffe_lrcn.git

# Install nano
RUN apt-get update && apt-get -y install nano

# Install pip
#RUN sudo apt-get update && sudo apt-get -y upgrade
#RUN sudo apt-get install -y python-pip

# Install Scipy libraries
#RUN python -m pip install --upgrade pip
#RUN pip install --user numpy scipy matplotlib ipython jupyter pandas sympy nose

