# User guide



{% hint style="danger" %}
Work in progress
{% endhint %}

### Prerequisites

Your data must have been registered to an atlas using [brainreg](../brainreg/introduction.md) \(or the brainreg-based registration within [cellfinder](../cellfinder/introduction.md).

Please follow the instructions for these packages, and ensure that the channel that you want to segment is downsampled \(e.g. using the `--downsample` flag in brainreg\).

## Usage

To load the software, just type `brainreg_segment` into your command window.

A [napari](https://github.com/napari/napari) viewer will then open, with some options for loading data:

![brainreg interface](../.gitbook/assets/brainreg_segment.png)

**To load your data**

There are three options for loading your data \(in the `Load data` section of the GUI\):

* `Load project (sample space)` - This is for loading a brainreg project in the coordinate space of your raw data \(i.e not warped to the atlas space\). N.B. the data will have been reoriented to the orientation of your chosen atlas, but it can be reoriented using the napari button in the bottom left \(a cube with an arrow above it\). **Click this button, then choose your brainreg \(or cellfinder registration\) output directory.**
* `Load project (sample space)` - As above, but the data loaded will have been warped into the atlas space. This is most useful when you want to visualise your segmented structures in [brainrender](https://github.com/BrancoLab/brainrender), as they must be in atlas space to do so. **Click this button, then choose your brainreg \(or cellfinder registration\) output directory.**
* `Load atlas` If you don't have your own data registered to the atlas, then you can just load the atlas. Useful for making visualisations etc. **Click this drop-down menu, then pick an atlas.**

\*\*\*\*

\*\*\*\*

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

