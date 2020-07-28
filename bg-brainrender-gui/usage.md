---
description: How to use BG-brainrender-GUI
---

# Usage

### Usage

You can **start** `brainrender-gui` directly from your terminal with the command

```text
brainrender-gui
```

Once the GUI is started it will open a window visualizing the `root` mesh of the atlas selected and several buttons to add and remove elements to the `brainrender` scene.

![bg-brainrender-GUI](../.gitbook/assets/app.png)

{% hint style="success" %}
To s**pecify which atlas to use:** use the **`-a`** argument when calling `brainrender-gui`:

```text
brainrender-gui -a allen_human_500um # the GUI will use the human atlas
```
{% endhint %}

### Adding actors

The first set of buttons is used to add elements to the `brainrender` scene:

* `Add brain regions`: clicking on this button opens a new window where  you can input the names of the brain regions to be added to the brainrender scene. 
* `Add cells`: clicking on this button opens a dialog to select and load a file containing cell coordinates data \(e.g. a `csv` file\). 
* `Add from file`: clicking on this button opens a dialog to select and load a file for a 3d mesh \(e.g. a `.obj` file\). 
* `Add sharptrack`: clicking on this button opens a dialog to select and load a `.m` file with the output of SHARPTRACK.



### Editing actors

Whenever an actor is added to the scene, its name will be added to the `Actors` list. The list can also be used to edit rendered actors:

* Double clicking an actor's name **will toggle the visibility** of the corresponding mesh. 
* A single click on an actor's name selects it for **editing** with **the `alpha`** \(transparency\) and **`color`** options below the actors list. Once an actor is selected from the `Actors` list, its color and alpha will appear in the text boxes below. Editing the values in these textboxes change the corresponding actor's properties.



### The hierarchy view

Pressing the `Show structures tree` button at the bottom right of the window shows a panel with the hierarchy view of brain regions in the selected atlas: ![](screenshots/app2.png)

![](../.gitbook/assets/app2.png)

The hierarchy view can be used to explore the structures hierarchy as well as to add brain regions to the scene: clicking on a region's tick box will add it to the list of actors in the scene. Press the same button again to hide the hierarchy view.

