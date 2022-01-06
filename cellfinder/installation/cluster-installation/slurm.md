---
description: Using cellfinder with the SLURM workload manager
---

# Installation with SLURM

These instructions are based on [SWC SLURM cluster](https://www.sainsburywellcome.org/web/content/scientific-computing), and so most of the command syntax will likely vary. Specifically, you are unlikely to have modules configured in exactly the same way as us.

{% hint style="info" %}
If you are from the SWC, and using the SWC cluster, please see the specific instructions [here](../../misc/using-cellfinder-at-the-swc.md).
{% endhint %}

## Prepare the environment

On our cluster, [modules](http://modules.sourceforge.net/) are only available on a compute node, so start an interactive job on a GPU node, and request a GPU for testing.

```bash
srun -p gpu --gres=gpu:1 --pty bash
```

Load miniconda

```bash
module load miniconda
```

## Set up conda environment and install cellfinder

Create and activate new minimal conda environment

```bash
  conda create --name cellfinder python=3.9
  conda activate cellfinder
```

Install CUDA and cuDNN. CUDA 11.2 and cuDNN 8.1 are recommended 

```bash
conda install -c conda-forge cudnn=8.1 cudatoolkit=11.2
```

Install cellfinder

```bash
  pip install cellfinder
```

Check that tensorflow and CUDA are configured properly:

```bash
  python
```

```python
import tensorflow as tf
tf.config.list_physical_devices('GPU')
```

If you see something like this, then all is well.

```python
2019-06-26 10:51:34.697900: I tensorflow/core/platform/cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX512F
2019-06-26 10:51:34.881183: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1432] Found device 0 with properties: 
name: TITAN RTX major: 7 minor: 5 memoryClockRate(GHz): 1.77
pciBusID: 0000:2d:00.0
totalMemory: 23.62GiB freeMemory: 504.25MiB
2019-06-26 10:51:34.881217: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1511] Adding visible gpu devices: 0
2019-06-26 10:51:35.251465: I tensorflow/core/common_runtime/gpu/gpu_device.cc:982] Device interconnect StreamExecutor with strength 1 edge matrix:
2019-06-26 10:51:35.251505: I tensorflow/core/common_runtime/gpu/gpu_device.cc:988]      0 
2019-06-26 10:51:35.251511: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1001] 0:   N 
2019-06-26 10:51:35.251729: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1115] Created TensorFlow device (/device:GPU:0 with 195 MB memory) -> physical GPU (device: 0, name: TITAN RTX, pci bus id: 0000:2d:00.0, compute capability: 7.5)
True
```

If you see something like this:

```python
2021-12-19 20:40:30.766514: W tensorflow/stream_executor/platform/default/dso_loader.cc:64] Could not load dynamic library 'libcudart.so.11.0'; dlerror: libcudart.so.11.0: cannot open shared object file: No such file or directory; LD_LIBRARY_PATH: /usr/local/cuda/lib64
```

CUDA and cuDNN cannot be found as `LD_LIBRARY_PATH` does not include the libraries installed by `conda`. Exit python 

Exit python

```python
exit()
```

Add the `lib` folder of your `conda` environement to the library path. 

```bash
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:~/.conda/envs/cellfinder/lib/
```

Restart python and test tensorflow again as described above. If it the error is gone, all should be fine.


Exit python

```python
exit()
```

End your interactive job

```bash
exit
```

## Running cellfinder

Once installed on a cluster with SLURM, cellfinder can be run interactively, but it is more convenient \(in the long run\) to submit a batch job.

A SLURM tutorial is out of scope of the cellfinder documentation \(look online or ask your sysadmin\), but an example batch script is here:

```bash
#!/bin/bash

#SBATCH -p gpu # partition (queue)
#SBATCH -N 1   # number of nodes
#SBATCH --mem 40G # memory pool for all cores
#SBATCH --gres=gpu:1
#SBATCH -n 10
#SBATCH -t 1-0:0 # time (D-HH:MM)
#SBATCH -o cellfinder.out
#SBATCH -e cellfinder.err
#SBATCH --mail-type=ALL
#SBATCH --mail-user=youremail@domain.com

cell_file='/path/to/signal/channel'
background_file='path/to/background/channel'
output_dir='/path/to/output/directory'

echo "Loading conda environment"
module load miniconda
conda activate cellfinder

echo "Running cellfinder"
# Just an example. See the user guide for the specific parameters
cellfinder -s $cell_file -b $background_file -o $output_dir -v 5 2 2 --orientation psl
```

You can then submit the batch job to the scheduler:

```bash
sbatch cellfinder_sbatch.sh
```

If you use the example script, you will receive an email when the job is done. To watch the progress, log onto a node with the same storage drive mounted and run:

```bash
watch tail -n 100 /path/to/cellfinder_log.log
```

