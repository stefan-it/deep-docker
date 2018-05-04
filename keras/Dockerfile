FROM nvidia/cuda:9.0-cudnn7-devel

RUN apt update && DEBIAN_FRONTEND=noninteractive apt install -y locales \
    graphviz python3-pip git-core

RUN sed -i -e 's/# de_DE.UTF-8 UTF-8/de_DE.UTF-8 UTF-8/' /etc/locale.gen && \
    dpkg-reconfigure --frontend=noninteractive locales && \
    update-locale LANG=de_DE.UTF-8

ENV LANG de_DE.UTF-8

RUN pip3 install tensorflow-gpu keras scikit-learn h5py gensim pandas \
    git+https://www.github.com/keras-team/keras-contrib.git
