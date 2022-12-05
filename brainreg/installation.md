---
description: Installing brainreg
---

# Installation

## Introduction

If you know what you're doing just run:

```bash
pip install brainreg
```

{% hint style="info" %}
If you're not completely sure what you're doing, read on.
{% endhint %}

## Requirements

The hardware requirements for brainreg depend on the atlas (and in particular the resolution) you want to use. Most machines (including laptops) will be able to use most of the atlases, but some atlases (such as the 10um mouse atlases) may need up to 32GB of RAM.

Currently brainreg works on Windows and Linux.&#x20;

## Setting up your machine

### Installing Python

brainreg is written in Python, and so needs a functional Python installation. Your machine may already have Python installed, but **I recommend installing miniconda**.

**See** [**Using conda**](../cellfinder/using-conda.md) **for details.**

{% hint style="danger" %}
brainreg should run on any type of Python installation, but if you don't use conda, I may not be able to help you.
{% endhint %}

## Installing brainreg

{% hint style="info" %}
Remember to activate your conda environment before doing anything
{% endhint %}

```bash
pip install brainreg
```

{% hint style="warning" %}
If you are using macOS then please run "`conda install -c conda-forge niftyreg"`
{% endhint %}
