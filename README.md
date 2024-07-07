# A simple, cross platform, modulith ecommerce system built on .NET Core [![Join the chat at https://gitter.im/simplcommerce/SimplCommerce](https://badges.gitter.im/simplcommerce/SimplCommerce.svg)](https://gitter.im/simplcommerce/SimplCommerce?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Build Status
| Build server    | Platform       | Status      |
|-----------------|----------------|-------------|
| Azure Pipelines | All            |[![Build Status](https://simplcommerce.visualstudio.com/simplcommerce/_apis/build/status/simplcommerce.SimplCommerce?branchName=master)](https://simplcommerce.visualstudio.com/simplcommerce/_build/latest?definitionId=1&branchName=master)
|Travis           | Linux / MacOS  |[![Build Status](https://travis-ci.org/simplcommerce/SimplCommerce.svg?branch=master)](https://travis-ci.org/simplcommerce/SimplCommerce) |

## Docker

For testing purpose only `docker run -p 5000:80 simplcommerce/ci-build`

Continuous deployment: https://ci.simplcommerce.com

## Visual Studio 2022 and SQL Server

#### Prerequisites

- SQL Server
- Visual Studio 2022 and .NET 8

#### Steps to run

- Update the connection string in appsettings.json in SimplCommerce.WebHost
- Build the whole solution.
- In Solution Explorer, make sure that SimplCommerce.WebHost is selected as the Startup Project
- Open the Package Manager Console Window and make sure that SimplCommerce.WebHost is selected as the Default project. Then type "Update-Database" then press "Enter". This action will create the database schema.
- In Visual Studio, press "Control + F5".
- The back-office can be accessed via /Admin using the following built-in account: admin@simplcommerce.com, 1qazZAQ!

## Mac/Linux with PostgreSQL

#### Prerequisite

- PostgreSQL
- [.NET Core SDK 8.0](https://www.microsoft.com/net/download/all)
- Entity Framework Core Tools (`dotnet tool install --global dotnet-ef`)

#### Steps to run

- Update the connection string in appsettings.json in SimplCommerce.WebHost.
- Run the simpl-build.sh file by issuing the following command: "sudo ./simpl-build.sh". For ubuntu 18: "sudo bash simpl-build.sh"
- In the terminal, navigate to "src/SimplCommerce.WebHost" and type "dotnet run" and then hit "Enter".
- Open http://localhost:49206 in the browser. The back-office can be accessed via /Admin using the following built-in account: admin@simplcommerce.com, 1qazZAQ!

## Technologies and frameworks used:

- ASP.NET Core
- Entity Framework Core
- ASP.NET Identity Core
- Angular 1.6.3
- MediatR 7.0.0 for domain event

## Docs

https://docs.simplcommerce.com/

## Roadmap

https://github.com/auroravirtuoso/e-commerce-system-dotnet/wiki/Roadmap

## How to contribute

- Star this project on GitHub.
- Report bugs or suggest features by creating new issues or adding comments to issues
- Submit pull requests
- Spread the word by blogging about SimplCommerce or sharing it on social networks
- Donate to us

## License

This project is licensed under the Apache 2.0 license.
