---
description: How to look at the registration results
---

# Visualisation

brainreg comes with a plugin \([napari-brainreg](https://github.com/brainglobe/napari-brainreg)\) for [napari](https://github.com/napari/napari)

To visualise your data, open napari and drag your brainreg output directory \(the one with the log file\) onto the napari window.

Various images should then open, including:

* `Image (downsampled)` - the image used for registration
* `Annotations` - the atlas labels, warped to your sample brain
* `Boundaries` - the boundaries of the atlas regions

If you downsampled additional channels, these will also be loaded.

![process](https://raw.githubusercontent.com/brainglobe/napari-brainreg/master/resources/napari-brainreg.png)

