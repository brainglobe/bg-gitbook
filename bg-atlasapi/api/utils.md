# utils

## Contents

* [**`check_internet_connection`** \[\#14\]](utils.md#check_internet_connection-14)
* [**`retrieve_over_http`** \[\#39\]](utils.md#retrieve_over_http-39)
* [**`conf_from_url`** \[\#71\]](utils.md#conf_from_url-71)
* [**`get_latest_atlases_version`** \[\#90\]](utils.md#get_latest_atlases_version-90)
* [**`read_json`** \[\#98\]](utils.md#read_json-98)
* [**`read_tiff`** \[\#104\]](utils.md#read_tiff-104)

## **`check_internet_connection`** \[\#14\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/utils.py#L14) online

```python
def check_internet_connection(url='http://www.google.com/', timeout=5,
    raise_error=True):
```

   
docstring:

```text
Check that there is an internet connection

url : str

url to use for testing (Default value = 'http://www.google.com/')

timeout : int

timeout to wait for [in seconds] (Default value = 5).

raise_error : bool

if false, warning but no error.
```

## **`retrieve_over_http`** \[\#39\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/utils.py#L39) online

```python
def retrieve_over_http(url, output_file_path):
```

   
docstring:

```text
Download file from remote location, with progress bar.

Parameters

----------

url : str

Remote URL.

output_file_path : str or Path

Full file destination for download.
```

## **`conf_from_url`** \[\#71\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/utils.py#L71) online

```python
def conf_from_url(url):
```

   
docstring:

```text
Read conf file from an URL.

Parameters

----------

url : str

conf file url (in a repo, make sure the "raw" url is passed)

Returns

-------

conf object
```

## **`get_latest_atlases_version`** \[\#90\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/utils.py#L90) online

```python
def get_latest_atlases_version():
```

   
docstring:

no docstring

## **`read_json`** \[\#98\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/utils.py#L98) online

```python
def read_json(path):
```

   
docstring:

no docstring

## **`read_tiff`** \[\#104\]

Check the [_**`source code`**_](https://github.com/brainglobe/bg-atlasapi/blob/master/bg_atlasapi/utils.py#L104) online

```python
def read_tiff(path):
```

   
docstring:

no docstring

