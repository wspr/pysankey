# pySankey

Uses matplotlib to create simple <a href="https://en.wikipedia.org/wiki/Sankey_diagram">
Sankey diagrams</a> flowing only from left to right.

[![Python package](https://github.com/AUMAG/pysankey/actions/workflows/python-package.yml/badge.svg)](https://github.com/AUMAG/pysankey/actions/workflows/python-package.yml)

[![Jekyll Pages](https://github.com/AUMAG/pysankey/actions/workflows/jekyll-gh-pages.yml/badge.svg)](https://github.com/AUMAG/pysankey/actions/workflows/jekyll-gh-pages.yml)

[![Coverage Status](https://coveralls.io/repos/github/AUMAG/pysankey/badge.svg?branch=master)](https://coveralls.io/github/AUMAG/pysankey?branch=master)

These will be the docs for the repository: https://aumag.github.io/pysankey/

## Minimal example

``` python
import pysankey as sky
import matplotlib.pyplot as plt
import pandas as pd

data = pd.DataFrame([
  (“a”,1.0,”ab”,2.0,”a”,1.0),
  (“a”,1.0,”ba”,0.8,”ba”,0.4),
  (“c”,1.5,”cd”,0.5,”d”,2.0),
  (“b”,0.5,”ba”,0.8,”ba”,0.4),
  (“b”,0.5,”ab”,0.8,”a”,1.0),
  (“d”,2.0,”cd”,0.4,”d”,1.0),
  (“e”,1.0,”e”,1.0,”e”,3.0),
])

plt.figure()
sky.sankey(
  data,
  sorting    = -1,
  titles    = [“Stage 1”,”Stage 2”,”Stage 3”],
  valign    = “center”,
)
plt.show()
```

## Requirements

Requires python3-tk (for python 3.x) you can
install the other requirements with:

``` bash
    pip install -r requirements.txt
```


## Package development

### Lint

	pylint pysankey

### Testing

	python -m pytest 

### Coverage

	coverage run -m pytest

