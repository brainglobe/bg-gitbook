# structure\_class

## Contents

* [**Structure**](structure_class.md#structure)
  * [**`__getitem__`** \[\#11\]](structure_class.md#__getitem__-11)
* [**StructuresDict**](structure_class.md#structuresdict)
  * [**`__init__`** \[\#39\]](structure_class.md#__init__-39)
  * [**`__getitem__`** \[\#51\]](structure_class.md#__getitem__-51)
  * [**`__repr__`** \[\#69\]](structure_class.md#__repr__-69)

## **Structure**

```text
Class implementing the lazy loading of a mesh if the dictionary is
queried for it.
```

### **`__getitem__`** \[\#11\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/structure_class.py#L11) online

```python
def __getitem__(self, item):
```

   
docstring:

no docstring

## **StructuresDict**

```text
Class to handle dual indexing by either acronym or id.

Parameters
----------
mesh_path : str or Path object
    path to folder containing all meshes .obj files
```

### **`__init__`** \[\#39\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/structure_class.py#L39) online

```python
def __init__(self, structures_list):
```

   
docstring:

no docstring

### **`__getitem__`** \[\#51\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/structure_class.py#L51) online

```python
def __getitem__(self, item):
```

   
docstring:

```text
Core implementation of the class support for different indexing.

Parameters

----------

item :

Returns

-------
```

### **`__repr__`** \[\#69\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/structure_class.py#L69) online

```python
def __repr__(self):
```

   
docstring:

```text
String representation of the class, print all regions names
```

