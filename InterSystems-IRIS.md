---
layout: default
title: InterSystems IRIS
nav_order: 2
---

# iris-driver-distribution
This repo provides drivers for use in making programmatic connections to InterSystems IRIS from Java (JDBC), Python (DB-API), C++ (ODBC), and .NET (ADO.NET). Programming a connection involves these simple steps:

1. Download the driver for the language you are developing in, as listed in **Drivers**. 
2. Follow the instructions in the learning content listed in **Get Started** to install it in your environment.
3. Continue with the instructions to add the appropriate connection string to your application. To do this, you'll need the following information about the InterSystems IRIS instance you want to connect to:
- The hostname or IP address of the instance's host and the superserver port of the instance (default 1972). If the instance is running in a container, you'll need to know what host port the superserver port was published as when the container was created.
- The Namespace you want to connect to.
- The username and password of an account with sufficient privileges to execute the actions you want to take through the connection.

## Drivers
- JDBC: 
**intersystems-jdbc-3.1.0.jar**
- DB-API: 
**intersystems_irispython-3.2.0-py3-none-any.whl**
-  ADO.NET:
**InterSystems.Data.IRISClient.dll**
- ODBC: 
In the **OBDC** folder, select **ODBC-2020.3.0.221.0-**_platform_identifier_, where _platform_identifier_ matches your platform.

## Get Started
- [Watch brief videos about connecting to IRIS Cloud](https://learning.intersystems.com/course/view.php?name=SQLaaSConnect)
- Read documentation about using drivers and connections strings:
	- [First Look: JDBC and InterSystems Databases](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_jdbc)
	- [Python DB-API Support](https://docs.intersystems.com/iris20221/csp/docbook/DocBook.UI.Page.cls?KEY=BTPI_pyapi)
	- [First Look: ADO.NET and InterSystems Products](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_adonet)
	- [First Look: ODBC and InterSystems Databases](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_odbc)
