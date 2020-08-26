# Specifying pixel size

For most tools, you must specify the pixel size of your data using command-line flags.

**You can specify them directly**

* `-x` or `--x-pixel-um` Pixel spacing of the data in the first dimension, specified in um.
* `-y` or `--y-pixel-um` Pixel spacing of the data in the second dimension, specified in um.
* `-z` or `--z-pixel-um` Pixel spacing of the data in the third dimension, specified in um.

**Or you can provide a supported metadata file**

* `--metadata` Metadata file containing pixel sizes \(any format supported by [micrometa](https://github.com/adamltyson/micrometa) can be used\).

{% hint style="info" %}
If both pixel sizes and metadata are provided, the command line arguments will take priority
{% endhint %}

