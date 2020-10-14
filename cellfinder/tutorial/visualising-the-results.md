---
description: How to inspect the results in napari
---

# Visualising the results

cellfinder comes with a plugin for [napari](https://napari.org/) for easily visualising the results. For more information see [Visualisation](../user-guide/visualisation.md). To quickly view your data:

* Open napari \(type `napari` into a command window\)
* Into the window then drag and drop:
  * The signal channel directory \(`test_brain/ch00`\)
  * The entire cellfinder output directory

![cellfinder results viewed in napari](../../.gitbook/assets/cellfinder_results.png)

The napari window then will then be populated with different layers \(left hand side\) that can be toggled:

* `ch00` The raw image data
* `allen_mouse_10um` The atlas annotations
* `Boundaries` The boundaries of the segmented regions
* `Non cells` The cell candidates classfied as artefacts \(blue\)
* `Cells` The cell candidates classified as cells \(yellow\)

{% hint style="info" %}
To make the results a bit more obvious when zoomed out, I've adjusted the contrast of the raw data \(`ch00`\), along with changing the symbol for the cells to `disc` and increasing the size.
{% endhint %}

These images are useful to assess how well cellfinder performed, but not much use for any kind of numerical analysis. To see what data is exported from cellfinder, take a look at [Exploring the numerical results](exploring-the-numerical-results.md).

