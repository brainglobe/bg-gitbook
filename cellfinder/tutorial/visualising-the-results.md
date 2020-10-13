---
description: How to inspect the results in napari
---

# Visualising the results

cellfinder comes with a plugin for [napari](https://napari.org/) for easily visualising the results. For more information see [Visualisation](../user-guide/visualisation.md). To quickly view your data:

* Open napari \(type `napari` into a command window\)
* Into the window then drag and drop:
  * The signal channel directory \(`test_brain/ch00`\)
  * The entire cellfinder output directory

The napari window then will then be populated with different layers \(left hand side\) that can be toggled:

* `ch00` The raw image data
* `allen_mouse_10um` The atlas annotations
* `Boundaries` The boundaries of the segmented regions
* `Non cells` The cell candidates classfied as artefacts
* `Cells` The cell candidates classified as cells 

