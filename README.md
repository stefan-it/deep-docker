# deep-docker

This repository contains various `Dockerfile`s for my deep learning research.
The built docker images can be started using [nvida-docker](https://github.com/NVIDIA/nvidia-docker).

The base image for all `Dockerfile`s is `nvidia/cuda`. The docker hub site can
be found [here](https://hub.docker.com/r/nvidia/cuda/).

## Building images and starting containers

To build any of the provided `Dockerfile`s go the relevant folder and execute:

```bash
docker build -t <desired-name-of-image> .
```

The image can be executed via `nvidia-docker`:

```bash
nvidia-docker run -it --rm <desired-name-of-image>
```

# Index

Currently, the following `Dockerfile`s exist:

## Keras

The `Dockerfile` for *Keras* uses *CUDA* in version 10.0 and *cudnn* in version
7. Thus, *TensorFlow* in version 1.8 can be used in combination with *Keras*.

Other useful libraries are also installed:

* `keras-contribu`
* `scikit-learn`
* `h5py`
* `gensim`
* `pandas`

## `pipenv`

The `Dockerfile` for `pipenv` and `pyenv` uses *CUDA* in version 10.0.

Here's a small `pyenv` example that installs Python 3.7:

```bash
root@5bc18bc97c62:/# pyenv install 3.7.0
Downloading Python-3.7.0.tar.xz...
-> https://www.python.org/ftp/python/3.7.0/Python-3.7.0.tar.xz
Installing Python-3.7.0...
Installed Python-3.7.0 to /.pyenv/versions/3.7.0
root@5bc18bc97c62:/# pyenv global 3.7.0
root@5bc18bc97c62:/# python --version
Python 3.7.0
```

## `pytorch`

The `Dockerfile` for `pytorch` 1.1.0 uses *CUDA* in version 10.1.