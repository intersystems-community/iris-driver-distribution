---
layout: default
title: Python
nav_order: 3
---
# Python

## Artifacts

| Artifact | Package | Documentation |
|----------|---------|---------------|
| DB-API driver | [`intersystems-irispython`](https://pypi.org/project/intersystems-irispython/) | [DB-API driver interface](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BPYDBAPI_about) |
| SQLAlchemy dialect | [`sqlalchemy-intersystems-iris`](https://pypi.org/project/sqlalchemy-intersystems-iris/) | [SQLAlchemy Dialect](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=GPYDEV_sqlalchemy) |

## Installation

Both packages are available from PyPI and install with [pip](https://pip.pypa.io/en/stable/installation/):

```shell
pip install intersystems-irispython
pip install sqlalchemy-intersystems-iris
```

You can also add these artifact names (one per line) to a `requirements.txt` file and install using

```shell
pip install -r requirements.txt
```

We recommend installing into a [virtual environment](https://docs.python.org/3/tutorial/venv.html).
