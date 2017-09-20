# Install Ubuntu 14.04 with CUDA 8
FROM kaixhin/cuda-caffe:8.0

# Install Ubuntu 16.04, CUDA 8 and cudnn 5, and miniconda3
#FROM  nvidia/cuda:8.0-cudnn5-runtime-ubuntu16.04
#FROM continuumio/miniconda3

RUN apt-get update && apt-get install -y sudo 

# Install wget and build-essential
#RUN apt-get update && apt-get install -y \
#    build-essential \
#    wget

# Install pip, python, and nano
RUN sudo apt-get update && sudo apt-get -y upgrade
RUN sudo apt-get install -y python-pip python-dev python-virtualenv \
    nano

# Install virtualenv
RUN pip install virtualenv

# Create a Python 2.7 environment in the style transfer directory 
# Note that this is not python 2.7.9, which was the version instructed to use.
RUN virtualenv -p python3 env 
#RUN /bin/bash -c "source env/bin/activate \
#    && pip install tensorflow-gpu keras"
