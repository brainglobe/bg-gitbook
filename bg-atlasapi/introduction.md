---
description: A lightweight python module to interact with atlases for systems neuroscience
---

# BG-AtlasAPI

Many excellent brain atlases exist for different species. Some of them have an API \(application programming interface\) to allow users to interact with the data programmatically \(e.g. the excellent [Allen Mouse Brain Atlas](www.brain-map.org)\), but many do not, and there is no consistent way to process data from multiple sources.

The brainglobe atlas API \(BG-AtlasAPI\) deals with this problem by providing a common interface for programmers to download and process data from multiple sources.

Each atlas consists of data files in a common format:

* A "reference" image of a brain \(`.tiff`\)
* An "annotation" image, with each brain region defined by a unique pixel value \(`.tiff`\)
* Meshes defining the surface of each brain region \(`.obj`\)
* A mapping of brain region pixel value to region name, and structure hierarchy \(`.json`\)
* Metadata defining the shape, orientation etc. of the data, and other info such as animal species and authors \(`.json`\)

### Atlases available

A number of atlases are in development, but those available currently are:

* The [Allen Mouse Brain Atlas](www.brain-map.org) at 10, 25 and 50 micron resolutions
* The [Allen Human Brain Atlas](www.brain-map.org) at 100 micron resolution
* The [Max Planck Zebrafish Brain Atlas](http://fishatlas.neuro.mpg.de) at 1 micron resolution
* The [Enhanced and Unified Mouse Brain Atlas](https://kimlab.io/brain-map/atlas/) at 25 micron resolution

### Installation

BG-AtlasAPI works with Python &gt;3.6, and can be installed from PyPI with:

```bash
pip install bg-atlasapi
```

