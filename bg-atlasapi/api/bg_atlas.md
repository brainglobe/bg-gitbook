# bg\_atlas

## Contents

* [Contents](bg_atlas.md#contents)
* [**BrainGlobeAtlas**](bg_atlas.md#brainglobeatlas)
  * [**`__init__`** \[\#45\]](bg_atlas.md#__init__-45)
  * [**`local_version`** \[\#87\]](bg_atlas.md#local_version-87)
  * [**`remote_version`** \[\#99\]](bg_atlas.md#remote_version-99)
  * [**`local_full_name`** \[\#119\]](bg_atlas.md#local_full_name-119)
  * [**`remote_url`** \[\#139\]](bg_atlas.md#remote_url-139)
  * [**`download_extract_file`** \[\#147\]](bg_atlas.md#download_extract_file-147)
  * [**`check_latest_version`** \[\#165\]](bg_atlas.md#check_latest_version-165)
  * [**`__repr__`** \[\#183\]](bg_atlas.md#__repr__-183)
* [**`_version_tuple_from_str`** \[\#13\]](bg_atlas.md#_version_tuple_from_str-13)
* [**`_version_str_from_tuple`** \[\#17\]](bg_atlas.md#_version_str_from_tuple-17)

## **BrainGlobeAtlas**

```text
Add remote atlas fetching and version comparison functionalities
to the core Atlas class.

Parameters
----------
atlas_name : str
    Name of the atlas to be used.
brainglobe_dir : str or Path object
    Default folder for brainglobe downloads.
interm_download_dir : str or Path object
    Folder to download the compressed file for extraction.
check_latest : bool (optional)
    If true, check if we have the most recent atlas (default=True). Set
    this to False to avoid waiting for remote server response on atlas
    instantiation and to suppress warnings.
print_authors : bool (optional)
    If true, disable default listing of the atlas reference.
```

### **`__init__`** \[\#45\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L45) online

```python
def __init__(self, atlas_name, brainglobe_dir=None,
    interm_download_dir=None, check_latest=True, print_authors=True):
```

   
docstring:

no docstring

### **`local_version`** \[\#87\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L87) online

```python
def local_version(self):
```

   
docstring:

```text
If atlas is local, return actual version of the downloaded files;

Else, return none.
```

### **`remote_version`** \[\#99\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L99) online

```python
def remote_version(self):
```

   
docstring:

```text
Remote version read from GIN conf file. If we are offline, return

None.
```

### **`local_full_name`** \[\#119\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L119) online

```python
def local_full_name(self):
```

   
docstring:

```text
As we can't know the local version a priori, search candidate dirs

using name and not version number. If none is found, return None.
```

### **`remote_url`** \[\#139\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L139) online

```python
def remote_url(self):
```

   
docstring:

```text
Format complete url for download.
```

### **`download_extract_file`** \[\#147\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L147) online

```python
def download_extract_file(self):
```

   
docstring:

```text
Download and extract atlas from remote url.
```

### **`check_latest_version`** \[\#165\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L165) online

```python
def check_latest_version(self):
```

   
docstring:

```text
Checks if the local version is the latest available

and prompts the user to update if not.
```

### **`__repr__`** \[\#183\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L183) online

```python
def __repr__(self):
```

   
docstring:

```text
Fancy print for the atlas providing authors information.
```

## **`_version_tuple_from_str`** \[\#13\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L13) online

```python
def _version_tuple_from_str(version_str):
```

   
docstring:

no docstring

## **`_version_str_from_tuple`** \[\#17\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/bg_atlas.py#L17) online

```python
def _version_str_from_tuple(version_tuple):
```

   
docstring:

no docstring

