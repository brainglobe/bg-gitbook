---
description: >-
  brainreg comes with a plugin for napari to allow you to easily view
  registration results.
---

# Visualisation

## Usage

### Sample space

Open napari and drag your [brainreg](https://github.com/brainglobe/brainreg) output directory \(the one with the log file\) onto the napari window.

Various images should then open, including:

* `Registered image` - the image used for registration, downsampled to atlas resolution
* `atlas_name` - e.g. `allen_mouse_25um` the atlas labels, warped to your sample brain
* `Boundaries` - the boundaries of the atlas regions

If you downsampled additional channels, these will also be loaded.

Some of these images will not be visible by default. Click the little eye icon to toggle visibility.

_N.B. If you use a high resolution atlas \(such as `allen_mouse_10um`\), then the files can take a little while to load._

![Visualisation in sample space](https://raw.githubusercontent.com/brainglobe/napari-brainreg/master/resources/sample_space.gif)

### Atlas space

`napari-brainreg` also comes with an additional plugin, for visualising your data in atlas space.

This is typically only used in other software, but you can enable it yourself:

* Open napari
* Navigate to `Plugins` -&gt; `Plugin Call Order`
* In the `Plugin Sorter` window, select `napari_get_reader` from the `select hook...` dropdown box
* Drag `brainreg_read_dir_standard_space` \(the atlas space viewer plugin\) above `brainreg_read_dir` \(the normal plugin\) to ensure that the atlas space plugin is used preferentially.

