---
description: Instructions and conventions for developing BrainGlobe projects
---

# Development

## Dependency support
Packages have to choose which versions of dependencies they officially support,
with minimum supported versions of each dependency used in continuous
integration testing. BrainGlobe projects should follow
[NEP 29 — Recommend Python and NumPy version support as a community policy
standard](https://numpy.org/neps/nep-0029-deprecation_policy.html) to
determine the **minimum** set of supported package versions:

- The last 42 months of Python releases
- The last 24 months of NumPy releases

In addition to this the last 24 months of other dependencies should also be
supported.


## Creating a development environment

It is recommended to use conda to install a development environment for
BrainGlobe projects. Once you have conda installed the following commands
will create and activate a conda environment with the requirements needed
for a development environment:

```
conda create -n brainglobe-dev -c conda-forge python=3.9 napari
conda activate brainglobe-dev
```

This installs packages that often can't be installed via. pip, including
`pyqt`. The specific version of Python is chosen to allow `tensorflow` to be
installed on macOS arm64 machines.

To install a specific BrainGlobe project for  development, clone the
GitHub repository, and then run

```
pip install -e '.[dev]'
```

from inside the repository. This will install the package, it's dependencies,
and it's development dependencies.
