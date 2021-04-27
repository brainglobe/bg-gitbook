---
description: About the cellfinder napari plugin
---

# Introduction

The algorithm that underlies the efficient cell detection in cellfinder is available for use as a plugin for [napari](https://napari.org/). This is a thin wrapper around the [cellfinder-core](../cellfinder-core/introduction.md) package and aims to:

* Provide the cell detection algorithm in a user-friendly form
* Allow the cell detection algorithm to be chained together with other tools in the Napari ecosystem
* Allow easier parameter optimisation for users of the other cellfinder tools.

{% hint style="info" %}
Eventually other tools in the BrainGlobe ecosystem \(e.g. [brainreg](../brainreg/introduction.md)\) will be developed as napari plugins to provide a full GUI for cell detection, atlas registration and downstream analysis.
{% endhint %}

![Visualising detected cells in the cellfinder napari plugin](../.gitbook/assets/napari-cellfinder.gif)

## Installation

First [install napari](https://napari.org/#installation). You can then install the plugin from within napari \(`Plugins` -&gt; `Install/Uninstall Package(s)`, choosing `cellfinder-napari`\). 

For analysis of larger images, please also ensure your GPU is set up properly \(see [Setting up your GPU](../cellfinder/installation/using-gpu.md)\).

## Usage

Please see the [User guide](user-guide.md).

