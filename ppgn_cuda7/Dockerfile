FROM kaixhin/cuda-caffe:7.0
MAINTAINER Socratic Datum <socratic.datum@gmail.com>

# Move to root and clone PPGN repo 
RUN git clone https://github.com/Evolving-AI-Lab/ppgn.git

# Clone the caffe_lrcn repo for image captioning (example 5)
RUN git clone https://github.com/anguyen8/caffe_lrcn.git
#RUN git clone https://github.com/thommiano/caffe_lrcn_joel.git

# Move into models folder and download
RUN cd /root/caffe/ppgn/nets/generator/noiseless && ./download.sh
RUN cd /root/caffe/ppgn/nets/caffenet && ./download.sh
RUN cd /root/caffe/ppgn/nets/placesCNN && ./download.sh
RUN cd /root/caffe/ppgn/nets/lrcn && ./download.sh

# Update packages and install image magic for command-line interfacees
RUN apt-get update && apt-get -y install imagemagick

# Install nano
RUN apt-get update && apt-get -y install nano

# Install virtualenv
RUN pip install virtualenv

# Create a Python 3 environment in the ppgn directory
RUN cd /root/caffe/ppgn && virtualenv -p python3 env

# Edit file path for caffe/python
RUN cd /root/caffe/ppgn && sed -i "s|/path/to/your/caffe/python|/root/caffe/python |g" settings.py

# Launch in ppgn directory/root/ppgn
WORKDIR /root/caffe/ppgn
