# User guide



{% hint style="danger" %}
Work in progress
{% endhint %}

### Prerequisites

Your data must have been registered to an atlas using [brainreg](../brainreg/introduction.md) \(or the brainreg-based registration within [cellfinder](../cellfinder/introduction.md).

Please follow the instructions for these packages, and ensure that the channel that you want to segment is downsampled \(e.g. using the `--downsample` flag in brainreg\).

## Usage

### Command line

```bash
    manual_region_seg "name_of_downsampled_image.nii" registration_directory
```

#### Arguments

Run `manual_region_seg -h` to see all options.

**Positional arguments**

* Downsampled image to be segmented, as a string \(e.g. `"downsampled.nii"`\)
* amap/cellfinder registration directory \(e.g.

  `/home/analysis/cellfinder_output/registration/`\)

**The following options may also be used:**

* `--preview` Preview the segmented regions in brainrender \(default:False\)
* `--volumes` Calculate the volume of each brain area included in the

  segmented region

* `--summarise` Summarise each region \(centers, volumes etc.\)
* `--shading` Object shading type for brainrender \(`flat`, `giroud` or `phong`\). Default: `flat`
* `--alpha` Object transparency for brainrender
* `--brush-size` Default size of the label brush.

### napari GUI

manual\_region\_seg will transform your image into standard space \(this may take a few minutes\) and then display the image in a [napari](https://github.com/napari/napari) viewer:

![manual\_seg\_window](https://raw.githubusercontent.com/SainsburyWellcomeCentre/neuro/master/resources/manual_segmentation_window.png)

**To segment regions:**

* Ensure that the "new\_region" tab is selected \(left hand side\)
* Rename this region \(by selecting the "new\_region" text\)
* Navigate to where you want to draw your region of interest.
  * Use the scroll bar at the bottom \(or left/right keys\) to navigate

    through the image stack

  * Use the mouse scrollwheel to zoom in or out
  * Drag with the mouse the pan the view
* Choose a brush size \(top left box\)
* Activate painting mode \(by selecting the paintbrush, top left\). You can

  go back to the navigation mode by selecting the magnifying glass.

* Colour in your region that you want to segment, ensuring that you make a

  solid object.

* Selecting the `ndim` toggle in the top left will extend the brush size in three dimensions \(so it will colour in multiple layers\).
* To add a new region press `Control+N`
* Repeat above for each region you wish to segment.
* Press `Alt-Q` on your keyboard to save the regions. If you used the `--preview flag`, once they are saved, they will be displayed in a brainrender window.

**Editing regions:**

If you have already run `manual_region_seg`, and run it again, the segmented regions will be shown. You can edit them, and press `Control+S` to resave them. If you don't want to save any changes, press `Control+X` to exit. The regions will still be previewed if you have selected that option.

