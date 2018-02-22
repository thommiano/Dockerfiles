#FROM goodfellow/competition:gpu

FROM ermaker/keras

RUN conda install -y \
    jupyter \
    matplotlib

RUN pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.2.0-cp27-none-linux_x86_64.whl

RUN conda install -y scikit-learn

RUN pip install python-igraph

RUN conda install -y pillow=3.4.1

RUN pip install --upgrade pip

RUN apt-get update
RUN apt-get install git-all -y

#RUN pip install -e git+https://github.com/tensorflow/cleverhans.git#egg=cleverhans
RUN pip install -qq -e git+http://github.com/tensorflow/cleverhans.git#egg=cleverhans

RUN pip install opencv-python
