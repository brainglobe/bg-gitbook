---
description: How to get your machine set up to work on cellfinder
---

# Setting up a development installation

{% hint style="info" %}
The instructions here are for the cellfinder repository, but the process is similar for all the others \(e.g. brainreg\).
{% endhint %}

To set up a development install, please fork the [cellfinder repository](https://github.com/SainsburyWellcomeCentre/cellfinder) and then:

Clone your fork

```text
git clone https://github.com/YOUR_USERNAME/cellfinder
cd cellfinder
```

Add the cellfinder repository as the upstream

```text
git remote add upstream https://github.com/SainsburyWellcomeCentre/cellfinder
```

Install an editable, development version of `cellfinder`

```text
pip install -e .[dev]
```

Finally, when working on cellfinder, keep your fork up to date

```text
git fetch upstream
git merge upstream/master
```

