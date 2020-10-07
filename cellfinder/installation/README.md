---
description: How to get cellfinder installed on your machine.
---

# Installation

## Introduction

If you know what you're doing \(and [your GPU is set up](setting-up-your-gpu.md)\), just run:

```bash
pip install cellfinder
```

{% hint style="info" %}
If you're not completely sure what you're doing, read on.
{% endhint %}

## Requirements

To run cellfinder you will need a relativelyfairlyfairly high-powered computer running Windows or Linux \(see [system requirements](system-requirements.md) for details\).

If you don't have access to a high-powered computer, your institute may have a compute cluster you can access. Get in touch with them, and forward them the [cluster installation](cluster-installation/) page.

For some aspects \(e.g. [setting up your GPU](setting-up-your-gpu.md)\), you may also need admin rights to your computer.

## Setting up your machine

Before installing cellfinder I recommend installing some other software first.

### Installing Python

cellfinder is written in Python, and so needs a functional Python installation. Your machine may already have Python installed, but **I recommend installing miniconda**.

**See** [**Using conda**](using-conda.md) **for details.**

{% hint style="danger" %}
cellfinder should run on any type of Python installation, but if you don't use conda, I may not be able to help you.
{% endhint %}

### Setting up your GPU

cellfinder doesn't need to use your GPU \(graphics card\), but if you have a supported card \(most recent NVIDIA cards\), it can run much, much faster with it.

**See** [**Setting up your GPU**](setting-up-your-gpu.md) **for details**

## Installing cellfinder

{% hint style="info" %}
Remember to activate your conda environment before doing anything
{% endhint %}

Open your terminal, and activate your conda environment

```bash
conda activate cellfinder
```

Then install cellfinder \(this could take a few minutes depending on the speed of your network connection\).

```bash
pip install cellfinder
```

## Download atlas and trained classification models \(optional\)

When you run cellfinder, it will download the files it needs \(atlas, trained machine learning models etc.\). If you want to save time later, or you know you won't have an internet connection when you run cellfinder, you can download these in advance. See [downloading files](downloading-files.md) for details.

