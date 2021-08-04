---
description: How to use the brainreg napari plugin
---

# User guide

## Getting started

To register your data, you will need a whole-brain image, i.e. not a part of a brain, and not some individual 2D sections. The format doesn't matter, as long as it can be loaded into napari, and the orientation etc. is dealt with by brainreg.

## Loading data

Loading your data into napari will vary depending on the data type, but with most types, you should be able to drag and drop your data into the main napari window. 

{% hint style="info" %}
If you are having trouble loading your data into napari, first check the [napari hub](https://www.napari-hub.org/) to see if there's a plugin to help. If that fails, go ahead and ask the nice people at the [image.sc](https://forum.image.sc/tag/napari) forum.
{% endhint %}

## Starting the plugin

Click `Plugins` at the top of the main napari window, and then click `brainreg-register: Atlas registration`. A new docked widget will appear in your napari window.

## Setting up registration

Choose the napari image layer you wish to be registered from `img layer`, along with the atlas you want to use from `Atlas key`. You must also set the voxel sizes in the axial \(z\) and in-plane \(x, y\) dimensions, along with the data orientation. The orientation is defined by three letters, based on [bg-space](https://github.com/brainglobe/bg-space), e.g. `psl`. For more details on this, see the outline [here](https://docs.brainglobe.info/cellfinder/image-orientation#orientation). Lastly, set a `registration output directory` \(where you want to save the data\).

{% hint style="warning" %}
Make sure that the image layer you are registering is not selected in the list of napari image layers on the left hand side. Any images that are selected, will also be registered along with the image layer chosen in `img layer`.
{% endhint %}

## Setting additional parameters

These parameters are the same as the brainreg command-line interface. For more details on these, see the documentation [here](https://docs.brainglobe.info/brainreg/user-guide/parameters).

