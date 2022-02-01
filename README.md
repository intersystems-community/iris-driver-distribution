# iris-driver-distribution
This repo provides drivers for use in making programmatic connections to IRIS Cloud from Java (JDBC), Python (DB-API), C++ (ODBC), and .NET (ADO.NET). Programming the connection involves these simple steps:

1. Download the driver for the language you are developing in, as listed in **Drivers**. 
2. Follow the instructions in the learning content listed in **Get Started** to install it in your environment.
3. Continue with the instructions to add the appropriate connection string to your application, using the connection information for your deployment. This information is displayed on the Deployment Details page in the Cloud Services Portal and includes:
	- Hostname and port
	- Namespace
	- IRIS username
    - The IRIS password you set when you created the deployment (not displayed for security)

# Drivers
- JDBC: 
**intersystems-jdbc-3.1.0.jar**
- DB-API: 
**intersystems_irispython-3.2.0-py3-none-any.whl**
-  ADO.NET:
**InterSystems.Data.IRISClient.dll**
- ODBC: 
In the **OBDC** folder, select **ODBC-2020.3.0.221.0-**_platform_identifier_, depending on your platform.

# Get Started
- [Watch brief videos about connecting to IRIS Cloud](https://learning.intersystems.com/course/view.php?name=SQLaaSConnect)
- Read documentation about using drivers and connections strings:
	- JDBC: [First Look: JDBC and InterSystems Databases](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_jdbc)
	- DB-API: [Python DB-API Support](https://docs.intersystems.com/iris20221/csp/docbook/DocBook.UI.Page.cls?KEY=BTPI_pyapi)
	- ADO.NET: [First Look: ADO.NET and InterSystems Products](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_adonet)
	- ODBC: [First Look: ODBC and InterSystems Databases](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_odbc)

