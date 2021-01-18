---
description: How to speed up cellfinder by using your GPU
---

# Setting up your GPU

## Introduction

**cellfinder** will run quite happily on your CPU, but the machine learning parts \(classifying cell candidates as cells or artefacts, and [Training the network](../user-guide/training/)\) **run much faster** using GPU.

### Requirements

The requirements are the same as those for [tensorflow GPU support](https://www.tensorflow.org/install/gpu), but essentially you need:

* A relatively modern **Windows or Linux based machine** \(unfortunately GPU acceleration on macOS is not supported\).
* An **NVIDIA GPU** with CUDA Compute Capability of 3.5 or higher \(see the list [here](https://en.wikipedia.org/wiki/CUDA)\) with at least 6GB memory. Basically any relatively expensive  NVIDIA GPU released in the last 5 years should be OK. So far, we've tested:
  * GTX 1070
  * GTX 1080
  * TITAN GTX
  * Quadro P5000
  * Quadro RTX 5000
  * RTX 2080
  * RTX 2080 \(laptop\)
  * TITAN RTX
* Someone who has the admin password and \(ideally\) **knows what they are doing** to install things.

## Installation

These instructions will vary somewhat between operating systems, and on how your machine is set up \(and how much control your institute will let you have\).

### Installing NVIDIA drivers

The first thing you definitely need are the drivers for your GPU, which can be downloaded [here](https://www.nvidia.com/download/index.aspx?lang=en-us). Hopefully, these will have been installed when your machine was set up, but for GPU support in cellfinder, you will need version **418.x or greater**.

### Installing CUDA and cuDNN

cellfinder uses [tensorflow](https://www.tensorflow.org/) which relies upon [CUDA](https://en.wikipedia.org/wiki/CUDA) and [cuDNN](https://developer.nvidia.com/cudnn). cellfinder requires **CUDA** and **cuDNN.**

CUDA and cuDNN are not too hard to install, but sometimes other software on your machine relies on different versions. It is possible to switch between the two, and it is easier if you are [using conda](../using-conda.md) \(see [here](https://blog.kovalevskyi.com/multiple-version-of-cuda-libraries-on-the-same-machine-b9502d50ae77)\). However, **I recommend that you** [**use conda**](../using-conda.md) **and install CUDA 11 and cuDNN 8 via conda.** On linux you can run:

```text
conda install cudatoolkit=11.0
conda install cudnn -c nvidia
```

This method is easier, and also doesn't require any admin rights \(useful on a cluster or shared machine\).

if this does not work for any reason, or you wish to have a system-wide installation of CUDA and cuDNN, then CUDA can be downloaded [here](https://developer.nvidia.com/cuda-toolkit-archive) and cuDNN from [here](https://developer.nvidia.com/cudnn). N.B. you will need to sign up for a \(free\) account to download cuDNN.

