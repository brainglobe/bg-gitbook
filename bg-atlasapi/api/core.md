# core

## Contents

* [**Atlas**](core.md#atlas)
  * [**`__init__`** \[\#28\]](core.md#__init__-28)
  * [**`resolution`** \[\#57\]](core.md#resolution-57)
  * [**`hierarchy`** \[\#63\]](core.md#hierarchy-63)
  * [**`lookup_df`** \[\#71\]](core.md#lookup_df-71)
  * [**`reference`** \[\#85\]](core.md#reference-85)
  * [**`annotation`** \[\#91\]](core.md#annotation-91)
  * [**`hemispheres`** \[\#97\]](core.md#hemispheres-97)
  * [**`hemisphere_from_coords`** \[\#122\]](core.md#hemisphere_from_coords-122)
  * [**`structure_from_coords`** \[\#148\]](core.md#structure_from_coords-148)
  * [**`_get_from_structure`** \[\#183\]](core.md#_get_from_structure-183)
  * [**`mesh_from_structure`** \[\#205\]](core.md#mesh_from_structure-205)
  * [**`meshfile_from_structure`** \[\#208\]](core.md#meshfile_from_structure-208)
  * [**`root_mesh`** \[\#211\]](core.md#root_mesh-211)
  * [**`root_meshfile`** \[\#214\]](core.md#root_meshfile-214)
  * [**`_idx_from_coords`** \[\#217\]](core.md#_idx_from_coords-217)
  * [**`get_structure_ancestors`** \[\#224\]](core.md#get_structure_ancestors-224)
  * [**`get_structure_descendants`** \[\#235\]](core.md#get_structure_descendants-235)

## **Atlas**

```text
Base class to handle atlases in BrainGlobe.

Parameters
----------
path : str or Path object
    path to folder containing data info.
```

### **`__init__`** \[\#28\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L28) online

```python
def __init__(self, path):
```

   
docstring:

no docstring

### **`resolution`** \[\#57\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L57) online

```python
def resolution(self):
```

   
docstring:

```text
Make resolution more accessible from class.
```

### **`hierarchy`** \[\#63\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L63) online

```python
def hierarchy(self):
```

   
docstring:

```text
Returns a Treelib.tree object with structures hierarchy.
```

### **`lookup_df`** \[\#71\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L71) online

```python
def lookup_df(self):
```

   
docstring:

```text
Returns a dataframe with id, acronym and name for each structure.
```

### **`reference`** \[\#85\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L85) online

```python
def reference(self):
```

   
docstring:

no docstring

### **`annotation`** \[\#91\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L91) online

```python
def annotation(self):
```

   
docstring:

no docstring

### **`hemispheres`** \[\#97\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L97) online

```python
def hemispheres(self):
```

   
docstring:

no docstring

### **`hemisphere_from_coords`** \[\#122\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L122) online

```python
def hemisphere_from_coords(self, coords, microns=False,
    as_string=False):
```

   
docstring:

```text
Get the hemisphere from a coordinate triplet.

Parameters

----------

coords : tuple or list or numpy array

Triplet of coordinates. Default in voxels, can be microns if

microns=True

microns : bool

If true, coordinates are interpreted in microns.

as_string : bool

If true, returns "left" or "right".

Returns

-------

int or string

Hemisphere label.
```

### **`structure_from_coords`** \[\#148\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L148) online

```python
def structure_from_coords(self, coords, microns=False,
    as_acronym=False, hierarchy_lev=None):
```

   
docstring:

```text
Get the structure from a coordinate triplet.

Parameters

----------

coords : tuple or list or numpy array

Triplet of coordinates.

microns : bool

If true, coordinates are interpreted in microns.

as_acronym : bool

If true, the region acronym is returned.

hierarchy_lev : int or None

If specified, return parent node at thi hierarchy level.

Returns

-------

int or string

Structure containing the coordinates.
```

### **`_get_from_structure`** \[\#183\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L183) online

```python
def _get_from_structure(self, structure, key):
```

   
docstring:

```text
Internal interface to the structure dict. It support querying with a

single structure id or a list of ids.

Parameters

----------

structure : int or str or list

Valid id or acronym, or list if ids or acronyms.

key : str

Key for the Structure dictionary (eg "name" or "rgb_triplet").

Returns

-------

value or list of values

If structure is a list, returns list.
```

### **`mesh_from_structure`** \[\#205\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L205) online

```python
def mesh_from_structure(self, structure):
```

   
docstring:

no docstring

### **`meshfile_from_structure`** \[\#208\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L208) online

```python
def meshfile_from_structure(self, structure):
```

   
docstring:

no docstring

### **`root_mesh`** \[\#211\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L211) online

```python
def root_mesh(self):
```

   
docstring:

no docstring

### **`root_meshfile`** \[\#214\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L214) online

```python
def root_meshfile(self):
```

   
docstring:

no docstring

### **`_idx_from_coords`** \[\#217\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L217) online

```python
def _idx_from_coords(self, coords, microns):
```

   
docstring:

no docstring

### **`get_structure_ancestors`** \[\#224\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L224) online

```python
def get_structure_ancestors(self, structure):
```

   
docstring:

```text
Returns a list of acronyms for all

ancestors of a given structure
```

### **`get_structure_descendants`** \[\#235\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/core.py#L235) online

```python
def get_structure_descendants(self, structure):
```

   
docstring:

```text
Returns a list of acronyms for all

descendants of a given structure
```

