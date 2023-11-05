# pokemon-review-app-clone

This project is a direct clone of a project from Youtube tutorial playlist **[ASP.NET Web API Tutorial 2022](https://www.youtube.com/playlist?list=PL82C6-O4XrHdiS10BLh23x71ve9mQCln0)** by [Teddy Smith](https://www.youtube.com/@TeddySmithDev).

The aim of this project is to get familiar with C# language and .NET framework. This is not a showcase project nor a representation of my work.

Target Framework: .NET 7

# Database

This project uses SQL Server from Microsoft. Database is run via Docker to have support in ARM macOS. Docker Desktop app must be installed and running to start the docker instance.

> Note: Rosetta2 must be enabled on macOS to run non-arm binaries.

Start docker instance:

```zsh
docker run --platform=linux/amd64 --name pokemonsql -e ACCEPT_EULA=1 -e MSSQL_SA_PASSWORD=PokemonSql123# -p 2022:1433 -d mcr.microsoft.com/mssql/server:2022-latest
```

After running this command, go to Docker Desktop, Containers and switch on `Only show running containers` to see actively running containers. A container with the name `pokemonsql` should appear.

Connection string after docker instance is running:

```
Server=localhost,2022;User Id=SA;Password=PokemonSql123#;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=15;
```
