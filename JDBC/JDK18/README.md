intersystems-jdbc-3.6.1.jar 
Intersystems IRIS Type 4 JDBC database driver; JDBC 4.2 specification from InterSystems IRIS Version 2022.2.0.368


Details about the jar files are extracted from here: https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BJAVA_config


The main InterSystems Java class packages are contained in the following files:

intersystems-jdbc-XXXX.jar — the core JDBC jar file. All of the other files in this list are dependent on this file.

In addition to the core JDBC API, this file also includes the classes that implement the Native SDK (see Using the Native SDK for Java).

intersystems-xep-XXXX.jar — required for XEP Java persistence applications (see Persisting Java Objects with InterSystems XEP). 
Depends on the JDBC jar.

intersystems-uima-XXXX.jar — required for UIMA support (see Using InterSystems UIMA). 
Depends on the JDBC jar.

intersystems-spark-XXXX.jar — required for the InterSystems implementation of the Apache Spark Data Source API (see Using the InterSystems Spark Connector). 
Depends on the JDBC jar.