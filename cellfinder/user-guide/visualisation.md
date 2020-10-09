---
description: >-
  cellfinder comes with a plugin for napari to allow you to easily view
  registration results.
---

# Visualisation

## Usage

### Getting started

To view your data, firstly open napari. The easiest way to do this is open a terminal \(making sure your cellfinder conda environment is activated\), then just type `napari`. A napari window should open.

### Visualising your raw data

Assuming that your raw data is stored as `.tiff` files, drag these into napari \(onto the main window in the middle\). This should be whatever you passed to cellfinder originally, i.e. a single multipage tiff, or a directory of 2D tiffs. You can load as many channels as you like \(e.g. the signal and the background channel\).

{% hint style="info" %}
The plugin does not yet support multi-channel analyses \(i.e. when you are detecting cells in &gt;1 channel\).
{% endhint %}

![Loading raw data into napari](../../.gitbook/assets/load_data.gif)

### Visualising your results

You can then drag and drop the cellfinder output directory \(the one you specified with the `-o` flag\) into the napari window. The plugin will then load your detected cells \(in yellow\) and the rejected cell candidates \(in blue\). If you carried out registration, then these results will be overlaid \(similarly to the [napari-brainreg](https://github.com/brainglobe/napari-brainreg) plugin, but transformed to the coordinate space of your raw data\).





{% hint style="danger" %}
This tool is deprecated, and will be replaced with a new visualisation tool.
{% endhint %}

To launch the viewer, run:

```text
cellfinder_view
```

A napari window will then open with two options \(`Load cellfinder project` and `Load amap project`\):

If you have run cellfinder, click `Load cellfinder project` and choose the directory set as the output folder. Alternatively, if you only want to inspect the registration, click `Load amap project` and choose either an amap output folder, or the `registration` directory of a cellfinder project.

Once a project has loaded, a number of buttons will appear on the right hand side of the window.

## **Data loading buttons**

{% hint style="info" %}
The buttons that appear will vary depending on the data that you have \(i.e. if you haven't run registration, that button won't appear\).
{% endhint %}

{% hint style="warning" %}
Be careful which data you load, as it may use a lot of RAM.
{% endhint %}

**Loading data:**

* `Load data directory` Load raw data as a directory of image files \(one image per plane\)
* `Load single image` Load raw data as a single multiplane image \(e.g. multiplane `.tif` or `.nii`.
* `Load downsampled data` Load the downsampled data channels from the registration step **\(usually the fastest approach\).**

**Adding results:**

* `Load registration` Loads the results of the registration including:
  * Annotations - image color coded by brain region. When this layer is highlighted \(using the panel on the left hand side\), you can hover the mouse over each brain region, and see its label in the bottom right hand side.
  * Boundaries - binary labels of the boundary of each brain region
* `Load cells` Loads the results of cell classification, including the cell candidates classified as cells, and those classified as non-cells. Once cells are loaded, a `Save cells` button will appear. If you add or delete cells \(using the buttons at the top left\), clicking this button will update the `cell_classification.xml` file. **Be careful, as this will overwrite the existing file.**

{% hint style="info" %}
Each part of the dataset will be loaded a "layer" which can be hidden, adjusted and reordered using the boxes on the left hand side. See the [napari tutorials](https://napari.org/tutorials/) for how to navigate the viewer.
{% endhint %}



