---
description: Downloading the files that cellfinder needs
---

# Downloading files

## Download atlas and trained classification models \(optional\)

When cellfinder runs, the appropriate machine learning models and reference atlas will be downloaded \(if not previously done so\). If you would like to download in advance to save time \(or if you will not have an internet connection\) you can run the following:

To download the machine learning model, run `cellfinder_download`

To download the atlas, please first run `brainglobe list` to see the list of available atlases, and then run `brainglobe install -a ATLAS_NAME` where `ATLAS_NAME` is the atlas you will use for cellfinder \(e.g. `allen_mouse_25um`\).

