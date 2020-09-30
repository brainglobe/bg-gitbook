# structure\_tree\_util

## Contents

* [**`child_ids`** \[\#6\]](structure_tree_util.md#child_ids-6)
* [**`get_structures_tree`** \[\#15\]](structure_tree_util.md#get_structures_tree-15)
* [**`add_descendants_to_tree`** \[\#19\]](structure_tree_util.md#add_descendants_to_tree-19)

## **`child_ids`** \[\#6\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/structure_tree_util.py#L6) online

```python
def child_ids(structure, structure_list):
```

   
docstring:

no docstring

## **`get_structures_tree`** \[\#15\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/structure_tree_util.py#L15) online

```python
def get_structures_tree(structures_list):
```

   
docstring:

```text
Creates a 'tree' graph with the hierarchical organisation of all
    structures
```

## **`add_descendants_to_tree`** \[\#19\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/structure_tree_util.py#L19) online

```python
def add_descendants_to_tree(structures_list, id_to_acronym_map, tree,
    structure_id, parent_id):
```

   
docstring:

```text
Recursively goes through all the the descendants of a region and adds
    them to the tree
```

