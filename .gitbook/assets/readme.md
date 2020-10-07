# cellfinder documentation

## Introduction

cellfinder is software from the [Margrie Lab](https://www.sainsburywellcome.org/web/groups/margrie-lab) at the [Sainsbury Wellcome Centre](https://www.sainsburywellcome.org/web/) for automated 3D cell detection and registration of whole-brain images \(e.g. serial two-photon or lightsheet imaging\).

![Detected labelled cells, overlaid on a segmented coronal brain section](https://cellfinder.info/images/cells.png)

It's a work in progress, but cellfinder can:

* Detect labelled cells in 3D in whole-brain images \(many hundreds of GB\)
* Register the image to an atlas \(such as the [Allen Mouse Brain Atlas](https://atlas.brain-map.org/atlas?atlas=602630314)\)
* Segment the brain based on the reference atlas
* Calculate the volume of each brain area, and the number of labelled cells within it
* Transform everything into standard space for analysis and visualisation

**For more information see the** [**website**](https://cellfinder.info) **or** [**GitHub repository**](https://github.com/SainsburyWellcomeCentre/cellfinder)

## Installation

```text
pip install cellfinder
```

{% hint style="info" %}
For detailed instructions see [Installation](installation/installation.md)
{% endhint %}

## Usage

To run the cell detection just do: 

```text
cellfinder -s signal_channel_images  optional_signal_channel_images -b background_channel_images -o /path/to/output_directory -x 2 -y 2 -z 5
```

{% hint style="info" %}
For more information and other options or analysis see [Getting started](user-guide/getting-started.md)
{% endhint %}

