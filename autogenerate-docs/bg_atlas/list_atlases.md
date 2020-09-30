# list\_atlases

## Contents

* [**`get_downloaded_atlases`** \[\#13\]](list_atlases.md#get_downloaded_atlases-13)
* [**`get_local_atlas_version`** \[\#32\]](list_atlases.md#get_local_atlas_version-32)
* [**`get_atlases_lastversions`** \[\#54\]](list_atlases.md#get_atlases_lastversions-54)
* [**`show_atlases`** \[\#83\]](list_atlases.md#show_atlases-83)

## **`get_downloaded_atlases`** \[\#13\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/list_atlases.py#L13) online

```python
def get_downloaded_atlases(with_version=False):
```

   
docstring:

```text
Get a list of all the downloaded atlases and their version.

Returns

-------

list

A list of tuples with the locally available atlases and their version
```

## **`get_local_atlas_version`** \[\#32\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/list_atlases.py#L32) online

```python
def get_local_atlas_version(atlas_name):
```

   
docstring:

```text
Get version of a downloaded available atlas.

Arguments

---------

atlas_name : str

Name of the atlas.

Returns

-------

str

Version of atlas.
```

## **`get_atlases_lastversions`** \[\#54\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/list_atlases.py#L54) online

```python
def get_atlases_lastversions():
```

   
docstring:

```text
Returns

-------

dict

A dictionary with metadata about already installed atlases.
```

## **`show_atlases`** \[\#83\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/list_atlases.py#L83) online

```python
def show_atlases(show_local_path=False):
```

   
docstring:

```text
Prints a formatted table with the name and version of local
    (downloaded)

and online (available) atlases. To do so, dowload info on

the latest atlas version and compares it with what it's stored

locally.

Arguments

---------

show_local_path : bool

If true, local path of the atlases are in the table with the rest

(optional, default=False).
```

