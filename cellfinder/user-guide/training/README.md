# Training the network

Cellfinder includes a pretrained network for cell candidate classification. This will likely need to be retrained for different applications. Rather than generate training data blindly, the aim is to reduce the amount of hands-on time by only generating training data where cellfinder classified a cell candidate incorrectly.

{% hint style="info" %}
If you don't have any data yet, and want to try out the training see [Using supplied training data](using-supplied-data.md)
{% endhint %}

## Generate training data

To generate training data, you will need:

* The cellfinder output file, `cell_classification.xml` \(it's in the `points` subdirectory\).
* The raw data used initially for cellfinder

To generate training data for a single brain, use `cellfinder_curate`:

```bash
cellfinder_curate signal_images background_images cell_classification.xml
```

### Arguments

* Signal images
* Background images
* `cell_classification.xml` file

{% hint style="info" %}
You must also specify the pixel sizes, see [Image definition](../../image-orientation.md#voxel-sizes)
{% endhint %}

**Optional**

* `-o` or `--output` Output directory for curation results. If this is not given, then the directory containing `cell_classification.xml` will be used.
* `--symbol` Marker symbol \(Default: `ring`\)
* `--marker-size` Marker size\(Default: `15`\)
* `--opacity` Marker opacity \(Default: `0.6`\)

A [napari](https://napari.org/) window will then open, showing two tabs on the left hand side:

* `Image` Selecting this allows you to change the contrast limits, to better visualise cells
* `Cell candidates` This shows the cell candidates than be curated. Cell

  candidates previously classified as cells are shown in yellow, and artifacts

  in blue.

By selecting the `Cell candidates` tab and then the cell selecting tool \(arrow at the top\), cell candidates can be selected \(either individually, or many by dragging the cursor\). There are then four keyboard commands:

* `C` Confirm the classification result, and add this to the training set
* `T` Toggle the classification result \(i.e. change the classification\),

  and add this to the training set.

* `Alt+Q` Save the results to an xml file
* `Alt+E` Finish curating the training dataset. This will carry out three operations:
  * Extract cubes around these points, into two directories \(`cells` and `non_cells`\).
  * Generate a yaml file pointing to these files for use with `cellfinder_train` \(see below\)
  * Close the viewer

Once a `yaml` file has been generated, you can proceed to training. However, it is likely useful to generate `yaml` files from additional datasets.

## Start training

You can then use these yaml files for training

{% hint style="warning" %}
_If you have any yaml files from previous versions of cellfinder, they will continue to work, but are not documented here. Just use them as you would the files from`cellfinder_curate`_
{% endhint %}

{% hint style="info" %}
If you would like to use the data that was originally used to train the supplied network, please see [Using supplied training data](using-supplied-data.md)
{% endhint %}

```bash
cellfinder_train -y yaml_1.yml  yaml_2.yml -o /path/to/output/directory/
```

### Arguments

* `-y` or `--yaml` The path to the yaml files defining training data
* `-o` or `--output` Output directory for the trained model \(or model weights\)

  results

**Optional**

* `--continue-training` Continue training from an existing trained model. If no model or model weights are specified, this will continue from the included model.
* `--trained-model` Path to a trained model to continue training
* `--model-weights` Path to existing model weights to continue training
* `--network-depth` Resnet depth \(based on [He et al. \(2015\)](https://arxiv.org/abs/1512.03385)\). Choose from

  \(18, 34, 50, 101 or 152\). In theory, a deeper network should classify better,

  at the expense of a larger model, and longer training time. Default: 50

* `--batch-size` Batch size for training \(how many cell candidates to process at once\). Default: 16
* `--epochs` How many times to use each sample for training. Default: 1000
* `--test-fraction` What fraction of data to keep for validation. Default: 0.1
* `--learning-rate` Learning rate for training the model
* `--no-augment` Do not use data augmentation
* `--save-weights` Only store the model weights, and not the full model. Useful to save storage space.
* `--no-save-checkpoints` Do not save the model after each training epoch. Useful to save storage space, if you are happy to wait for the chosen number of epochs to complete. Each model file can be large, and if you don't have much training data, they can be generated quickly.
* `--tensorboard` Log to `output_directory/tensorboard`. Use `tensorboard --logdir outputdirectory/tensorboard` to view.
* `--save-progress` Save training progress to a .csv file \(`output_directory/training.csv`\).

### Further help

All `cellfinder_train` options can be found by running:

```bash
cellfinder_train -h
```

