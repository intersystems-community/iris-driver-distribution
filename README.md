# InterSystems IRIS client artifacts

This repository lists the client libraries and drivers InterSystems offers for connecting applications to InterSystems IRIS, organized by programming language, and describes how to install them or use them in your projects.

- [Java, including JDBC](#java)
- [Python, including DB-API](#python)
- [.NET](#net)
- [Node.js](#nodejs)
- [ODBC](#odbc)

For general documentation on how to use these artifacts, see the official [InterSystems documentation on connecting to InterSystems IRIS](https://docs.intersystems.com/components/csp/docbook/DocBook.UI.Page.cls?KEY=GDRIVE_intro).

> [!IMPORTANT]
> These client artifacts are currently still included in regular installations of InterSystems IRIS, in some subdirectory of `install-dir/dev/`, but this delivery model will be phased out by the end of 2027. From that point on, the client artifacts will only be available through the direct distribution channels described below.

> [!NOTE]
> Previous versions of this repository included copies of several additional client artifacts. These are now available through secure, direct distribution channels as described below, including the latest versions compatible with your IRIS server version. 
> We are no longer maintaining copies of such artifacts on this page.

## Java

Java client artifacts are published to Maven Central under the [`com.intersystems`](https://mvnrepository.com/artifact/com.intersystems) group ID.

### Artifacts

| Artifact | Maven coordinates | Documentation |
|----------|-------------------|---------------|
| JDBC driver | [`com.intersystems:intersystems-jdbc`](https://mvnrepository.com/artifact/com.intersystems/intersystems-jdbc) | [JDBC Driver Support](https://docs.intersystems.com/iris20221/csp/docbook/DocBook.UI.Page.cls?KEY=BTPI_jdbc) |
| XEP driver | [`com.intersystems:intersystems-xep`](https://mvnrepository.com/artifact/com.intersystems/intersystems-xep) | [Using XEP with Java](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BJAVXEP_preface) |
| Document API | [`com.intersystems:intersystems-document`](https://mvnrepository.com/artifact/com.intersystems/intersystems-document) | [InterSystems Document API](https://docs.intersystems.com/services/csp/docbook/DocBook.UI.Page.cls?KEY=CDOCDRIVERS_intro) |

### Installing Maven

These artifacts are normally consumed through [Apache Maven](https://maven.apache.org/), a build tool that downloads dependencies for you. If you don't have it yet:

- [Download Maven](https://maven.apache.org/download.cgi)
- [Installation instructions](https://maven.apache.org/install.html)
- [Maven in 5 minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)

Check your installation with `mvn -version`.

### Adding the artifacts to your project

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

### Downloading a jar file from the command line

To fetch a library as a plain jar file without setting up a project, use the Maven dependency plugin. This example downloads the JDBC driver into the current directory:

```shell
mvn dependency:copy -Dartifact=com.intersystems:intersystems-jdbc:3.11.0 -DoutputDirectory=.
```

Change the coordinates to download the XEP driver or the Document API instead.

### Hibernate

InterSystems IRIS is supported by Hibernate ORM starting with Hibernate 7.4. This support is part of Hibernate itself and is not available as a separate artifact. See [Hibernate API](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BTPI_hibernate) in the InterSystems documentation.

## Python

### Artifacts

| Artifact | Package | Documentation |
|----------|---------|---------------|
| DB-API driver | [`intersystems-irispython`](https://pypi.org/project/intersystems-irispython/) | [DB-API driver interface](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BPYDBAPI_about) |
| SQLAlchemy dialect | [`sqlalchemy-intersystems-iris`](https://pypi.org/project/sqlalchemy-intersystems-iris/) | [SQLAlchemy Dialect](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=GPYDEV_sqlalchemy) |

### Installation

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

## .NET

.NET artifacts are published on [NuGet](https://www.nuget.org/).

### Artifacts

| Artifact | NuGet package | Documentation |
|----------|---------------|---------------|
| ADO.NET | [`InterSystems.Data.IRISClient`](https://www.nuget.org/packages/InterSystems.Data.IRISClient/) | [ADO.NET Managed Provider](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BNET_ado), [Native SDK for .NET](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BNETNAT_about) |
| Entity Framework Core | [`InterSystems.EntityFrameworkCore.Iris`](https://www.nuget.org/packages/InterSystems.EntityFrameworkCore.Iris/) | _To be added_ |
| XEP | [`InterSystems.Data.XEP`](https://www.nuget.org/packages/InterSystems.Data.XEP/) | [Introduction to XEP for .NET](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BNETXEP_intro) |
| Document API | [`InterSystems.Data.Document`](https://www.nuget.org/packages/InterSystems.Data.Document/) | [InterSystems Document API](https://docs.intersystems.com/services/csp/docbook/DocBook.UI.Page.cls?KEY=CDOCDRIVERS_intro) |
| .NET binding | [`InterSystems.Data.Bindings`](https://www.nuget.org/packages/InterSystems.Data.Bindings/) | _Deprecated, see below for details_ |

> [!IMPORTANT]
> InterSystems recommends using Entity Framework or ADO.NET for building Object-oriented applications in .NET.
> The .NET Binding option previously included with Caché and Ensemble is [discontinued](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=GCRN_discontinued_features) on IRIS, and available for compatibility purposes only, with support on a best-effort basis. [Documentation for the .NET binding](https://docs.intersystems.com/latest/csp/docbook/DocBook.UI.Page.cls?KEY=GBMP_proxy) is only available in the Caché and Ensemble documentation library.

### Installation

Install a package with the [.NET CLI](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-add-package):

```shell
dotnet add package InterSystems.Data.IRISClient
```

or from the Visual Studio Package Manager Console:

```powershell
Install-Package InterSystems.Data.IRISClient
```

Replace the package name with any of the packages listed above.

## Node.js

### Artifacts

| Artifact | npm package | Documentation |
|----------|-------------|---------------|
| Native SDK for Node.js | [`@intersystems/intersystems-iris-native`](https://www.npmjs.com/package/@intersystems/intersystems-iris-native) | [Node.js driver](https://docs.intersystems.com/irislatest/csp/docbook/Doc.View.cls?KEY=PAGE_nodejs_native) |

### Installing npm

`npm` is the package manager that comes with [Node.js](https://nodejs.org/). If you don't have it yet:

- [Download and install Node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

Check your installation with `node -v` and `npm -v`.

### Installation

```shell
npm install @intersystems/intersystems-iris-native
```

## ODBC

There is no specific standard repository for distributing ODBC drivers. We recommend downloading them from the [InterSystems download portal](https://downloads.intersystems.com/components). See the [InterSystems Documentation](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BNETODBC_intro) for more about establishing ODBC connections.

> [!NOTE]
> We occasionally make recent copies of the ODBC driver available through this repository for users of our community edition or cloud services that do not yet have an InterSystems SSO account.
> This is on a courtesy basis only and not a commitment.