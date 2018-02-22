from nvidia/cuda:8.0-cudnn7-runtime-ubuntu16.04

#FROM ermaker/keras
RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    build-essential \
    curl \
    git \
  && rm -rf /var/lib/apt/lists/*

RUN curl -qsSLkO \
    https://repo.continuum.io/miniconda/Miniconda-latest-Linux-`uname -p`.sh \
  && bash Miniconda-latest-Linux-`uname -p`.sh -b \
  && rm Miniconda-latest-Linux-`uname -p`.sh

ENV PATH=/root/miniconda2/bin:$PATH

RUN conda install -y \
    h5py \
    pandas \
    theano \
  && conda clean --yes --tarballs --packages --source-cache \
  && pip install --upgrade -I setuptools \
  && pip install --upgrade \
    keras \
    https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.9.0rc0-cp27-none-linux_x86_64.whl

RUN conda install -y \
    jupyter \
    matplotlib \
    seaborn

# RUN pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.2.0-cp27-none-linux_x86_64.whl
RUN pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.4.0-cp27-none-linux_x86_64.whl

RUN conda install -y scikit-learn

RUN conda install -c conda-forge librosa

RUN conda install -c mutirri -y blessings=1.6

RUN conda install -c conda-forge tqdm=4.14.0

RUN pip install python-igraph

RUN conda install -y pillow=3.4.1
