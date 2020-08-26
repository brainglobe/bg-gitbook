# Introduction

## About

brainreg is an update to [amap](https://github.com/SainsburyWellcomeCentre/amap-python) \(itself a port of the [original Java software](https://www.nature.com/articles/ncomms11879)\) to include multiple registration backends, and to support the many atlases provided by [bg-atlasapi](https://github.com/brainglobe/bg-atlasapi).

Currently the only registration backend is [NiftyReg](http://cmictig.cs.ucl.ac.uk/wiki/index.php/NiftyReg).

## Details

The aim of brainreg is to register the template brain \(e.g. from the [Allen Reference Atlas](https://mouse.brain-map.org/static/atlas)\) to the sample image. Once this is complete, any other image in the template space can be aligned with the sample \(such as region annotations, for segmentation of the sample image\). The template to sample transformation can also be inverted, allowing sample images to be aligned in a common coordinate space.

To do this, the template and sample images are filtered, and then registered in a three step process \(reorientation, affine registration, and freeform registration.\) The resulting transform from template to standard space is then applied to the atlas.

Full details of the process are in the [original paper](https://www.nature.com/articles/ncomms11879).

![Overview of the registration process](https://raw.githubusercontent.com/SainsburyWellcomeCentre/amap-python/master/resources/reg_process.png)

## Installation

```bash
pip install brainreg
```

{% hint style="info" %}
For detailed instructions see [Installation](installation.md)
{% endhint %}

## Usage

```bash
brainreg /path/to/raw/data /path/to/output/directory -x 2 -y 2 -z 5
```

{% hint style="info" %}
For more information see [User guide](user-guide/) or try out the [Tutorial](tutorial.md)
{% endhint %}

