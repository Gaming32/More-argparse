# Intro
## Getting Started
### Installing
First install with:
``` shell
$ python3 -m pip install more-argparse
```
### Importing
Then you import it with either:
``` python
import argparse
import margparse
```
or
``` python
from argparse import *
from margparse import *
```
It's important that you do the same for both.
### Checking the Contents of margparse
First, open a Python interactive session:
``` shell
$ python3
```
Then, import it and check the contents:
``` python
>>> import margparse
>>> dir(margparse)
['GlobbingType', '__all__', '__author__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__path__', '__spec__', '__version__', '_actions_all', '_types_all', 'actions', 'types']
```

# Contents
## Types
### GlobbingType
If the argument is a glob, glob the argument and add each filename to a list as `basetype(filename)`, otherwise return `[basetype(argument)]`

#### Arguments

Name    | Type    | Description
------- | ------- | -----------
basetype | callable | see above; use case: `basetype=argparse.FileType('r')`
recursive | bool | passed to glob.glob