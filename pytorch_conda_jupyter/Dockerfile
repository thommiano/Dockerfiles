from nvidia/cuda:8.0-cudnn7-runtime-ubuntu16.04
from continuumio/miniconda:latest

# Create conda env
RUN conda create -n pytorch_conda_env python=2.7.13
#RUN conda create -n pytorch_conda_env python=3.6
#RUN conda create -n pytorch_conda_env python=3.5
RUN /bin/bash -c "source activate pytorch_conda_env \
    && conda install jupyter \
    && conda install tqdm \
    && conda install matplotlib \
    && conda install pytorch torchvision cuda80 -c soumith"
