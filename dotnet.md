---
layout: default
title: .NET
nav_order: 4
---
# .NET

.NET artifacts are published on [NuGet](https://www.nuget.org/).

## Artifacts

| Artifact | NuGet package | Documentation |
|----------|---------------|---------------|
| ADO.NET | [`InterSystems.Data.IRISClient`](https://www.nuget.org/packages/InterSystems.Data.IRISClient/) | [Native SDK for .NET](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BNETNAT_about) |
| Entity Framework Core | [`InterSystems.EntityFrameworkCore.Iris`](https://www.nuget.org/packages/InterSystems.EntityFrameworkCore.Iris/) | _To be added_ |
| XEP | [`InterSystems.Data.XEP`](https://www.nuget.org/packages/InterSystems.Data.XEP/) | [Introduction to XEP for .NET](https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=BNETXEP_intro) |
| Document API | [`InterSystems.Data.Document`](https://www.nuget.org/packages/InterSystems.Data.Document/) | [InterSystems Document API](https://docs.intersystems.com/services/csp/docbook/DocBook.UI.Page.cls?KEY=CDOCDRIVERS_intro) |
| .NET binding | [`InterSystems.Data.Bindings`](https://www.nuget.org/packages/InterSystems.Data.Bindings/) | This library is available for compatibility purposes only. InterSystems recommends using Entity Framework for new projects. |

## Installation

Install a package with the [.NET CLI](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-add-package):

```shell
dotnet add package InterSystems.Data.IRISClient
```

or from the Visual Studio Package Manager Console:

```powershell
Install-Package InterSystems.Data.IRISClient
```

Replace the package name with any of the packages listed above.
