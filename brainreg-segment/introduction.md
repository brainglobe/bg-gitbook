---
description: Manually segment 1/2/3D structures for volumetric analysis
---

# Introduction

brainreg-segment is a companion to [brainreg](../brainreg/introduction.md) allowing manual segmentation of regions/objects within the brain \(e.g. injection sites, probes etc.\) allowing for automated analysis of brain region distribution, and visualisation \(e.g. in [brainrender](https://github.com/BrancoLab/brainrender)\).

### Installation

brainreg-segment comes bundled with brainreg, so see the [brainreg installation instructions](../brainreg/installation.md). brainreg-segment can be installed on it's own \(see below\), but you will need to register your data with brainreg first. 

### Usage

See [User guide](user-guide.md).

### Standalone installation

If you don't want to install brainreg, brainreg-segment can be installed on its own. brainreg-segment is distributed as a plugin for [napari](https://napari.org/), so first follow the [napari installation instructions](https://napari.org/). You can then install `brainreg-segment` from the  napari plugin menu.

![Installing from the napari plugin menu](../.gitbook/assets/install_plugin.png)

Alternatively, the plugin can be installed into a Python environment with `pip install brainreg-segment`.

