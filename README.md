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

The `Dockerfile` for *Keras* uses *CUDA* in version 9.0 and *cudnn* in version
7. Thus, *TensorFlow* in version 1.5 can be used in combination with *Keras*.

Other useful libraries are also installed:

* `scikit-learn`
* `h5py`
* `gensim`
* `pandas`