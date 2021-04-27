---
description: How to use the cellfinder napari plugin.
---

# User guide

The cellfinder algorithm is in two stages. Firstly, cell candidates \(objects of roughly the correct size and intensity to be a cell\) are detected, and then a deep learning network classifies these cell candidates as being cells or artefacts. Because this classification step will need to be retrained for new data, the napari plugin is split into three sections:  


* [Cell detection](cell-detection/)
* [Training data generation](training-data-generation.md)
* [Training the network](training-the-network.md)

{% hint style="info" %}
To understand how cellfinder works, it may be useful to take a look at the [preprint](https://www.biorxiv.org/content/10.1101/2020.10.21.348771v2). 
{% endhint %}

