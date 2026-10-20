---
layout: default
title: Java
nav_order: 2
---
# Java

Java client artifacts are published to Maven Central under the [`com.intersystems`](https://mvnrepository.com/artifact/com.intersystems) group ID.

## Artifacts

| Artifact | Maven coordinates | Documentation |
|----------|-------------------|---------------|
| JDBC driver | [`com.intersystems:intersystems-jdbc`](https://mvnrepository.com/artifact/com.intersystems/intersystems-jdbc) | [JDBC Driver Support](https://docs.intersystems.com/iris20221/csp/docbook/DocBook.UI.Page.cls?KEY=BTPI_jdbc) |
| XEP driver | [`com.intersystems:intersystems-xep`](https://mvnrepository.com/artifact/com.intersystems/intersystems-xep) | [Using XEP with Java](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BJAVXEP_preface) |
| Document API | [`com.intersystems:intersystems-document`](https://mvnrepository.com/artifact/com.intersystems/intersystems-document) | [InterSystems Document API](https://docs.intersystems.com/services/csp/docbook/DocBook.UI.Page.cls?KEY=CDOCDRIVERS_intro) |

## Installing Maven

These artifacts are normally consumed through [Apache Maven](https://maven.apache.org/), a build tool that downloads dependencies for you. If you don't have it yet:

- [Download Maven](https://maven.apache.org/download.cgi)
- [Installation instructions](https://maven.apache.org/install.html)
- [Maven in 5 minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)

Check your installation with `mvn -version`.

## Adding the artifacts to your project

Copy the dependency you need into the `<dependencies>` section of your `pom.xml`. Check the Maven Central pages linked above for the latest version of each artifact.

**JDBC driver**

```xml
<dependency>
    <groupId>com.intersystems</groupId>
    <artifactId>intersystems-jdbc</artifactId>
    <version>3.11.0</version>
</dependency>
```

**XEP driver**

```xml
<dependency>
    <groupId>com.intersystems</groupId>
    <artifactId>intersystems-xep</artifactId>
    <version>TBC</version>
</dependency>
```

**Document API**

```xml
<dependency>
    <groupId>com.intersystems</groupId>
    <artifactId>intersystems-document</artifactId>
    <version>1.0.3</version>
</dependency>
```

## Downloading a jar file from the command line

To fetch a library as a plain jar file without setting up a project, use the Maven dependency plugin. This example downloads the JDBC driver into the current directory:

```shell
mvn dependency:copy -Dartifact=com.intersystems:intersystems-jdbc:3.11.0 -DoutputDirectory=.
```

Change the coordinates to download the XEP driver or the Document API instead.

## Hibernate

InterSystems IRIS is supported by Hibernate ORM starting with Hibernate 7.4. This support is part of Hibernate itself and is not available as a separate artifact. See [Hibernate API](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BTPI_hibernate) in the InterSystems documentation.
