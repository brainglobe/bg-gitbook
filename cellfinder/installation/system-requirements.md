---
description: What do you need to run cellfinder
---

# System requirements

## Operating system

Any recent Windows or Linux system should work, but only these operating systems have been tested so far:

* Ubuntu 16.04
* Ubuntu 18.04
* Windows 10

{% hint style="warning" %}
macOS should work, but only Windows and Linux are fully supported
{% endhint %}

## Hardware requirements

cellfinder will run on most recent computer hardware, and the requirements vary somewhat on the size of the data you have, but for big images, it can be pretty slow \(4-8 hours\). So I recommend:

* Multicore CPU \(the more cores and the faster the better\)
* A recent NVIDIA GPU \(the more VRAM and CUDA cores the better\). Optional, but see [setting up your GPU](setting-up-your-gpu.md) for details.
* Plenty of RAM. If you want to register your images to an atlas, this can use up to 25GB of RAM \(depending on the atlas\)
* Fast local storage for your data \(ideally SSD\)

