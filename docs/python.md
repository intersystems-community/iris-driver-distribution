---
layout: default
title: Python Driver
nav_order: 2
---

# Python Driver

The python driver is called native API.

There is two version of this driver:

* offical python driver
* community python driver

## Official Python Driver

The official python driver is the one that is maintained by InterSystems.

It can be downloaded from this [github](https://github.com/intersystems-community/iris-driver-distribution).

### Installation

The driver can be installed using pip:

```bash
pip install https://github.com/intersystems-community/iris-driver-distribution/raw/main/DB-API/intersystems_irispython-3.2.0-py3-none-any.whl
```

### requirements.txt

```txt
https://github.com/intersystems-community/iris-driver-distribution/raw/main/DB-API/intersystems_irispython-3.2.0-py3-none-any.whl
```

### Usage

```python
import irisnative

# Create a connection
connection = irisnative.createConnection("localhost", 1792, "USER", "superuser", "SYS", sharedmemory = True)

# Create a cursor
cursor = connection.cursor()

# Execute a query
cursor.execute("SELECT 1")

# Fetch the result
result = cursor.fetchall()

# Print the result
print(result)

# Close the connection
connection.close()
```

## Community Python Driver

The community python driver is the one that is maintained by the community.

It can be downloaded from this [github](https://github.com/intersystems-community/iris-driver-distribution).

It has the same API as the official python driver but it supports more features like:

* more complete support of DB-API
* SQLAlchemy support
* some bug fixes and enhancements (stream support, etc.)

### Installation

The driver can be installed using pip:

```bash
pip install https://github.com/intersystems-community/iris-driver-distribution/raw/main/DB-API/intersystems_iris-3.3.0-py3-none-any.whl
```

### requirements.txt

```txt
https://github.com/intersystems-community/iris-driver-distribution/raw/main/DB-API/intersystems_iris-3.3.0-py3-none-any.whl
```

### Usage

```python
import intersystems_iris

# Create a connection
connection = intersystems_iris.createConnection("localhost", 51773, "USER", "superuser", "SYS", sharedmemory = True)

# Create a cursor
cursor = connection.cursor()

# Execute a query
cursor.execute("SELECT 1")

# Fetch the result
result = cursor.fetchall()

# Print the result
print(result)

# Close the connection
connection.close()
```
