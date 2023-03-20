# Dotnet Command Documentation
More information on commands can be found at [Dotnet CLI Overview](https://learn.microsoft.com/en-us/dotnet/core/tools/)

## Dev Certs

### Trust

Trust local development certs from Microsoft

`dotnet dev-certs https --trust`

```
dotnet dev-certs https --trust
```

## Project and Solution

### List Project Templates

Lists all installed dotnet solution and project templates

`dotnet new --list`

```
dotnet new --list
```

### New

Creates a new solution or project

`dotnet new <template> -lang <launguage> --name <name>`

```
dotnet new webapi -lang "C#" --name "my_solution"
```

> --name can be replaced with -n

```
dotnet new webapi -lang "C#" --n my_solution
```

### Solution Add

Add an existing project or multiple projects to an existing solution

`dotnet sln add <project>`

```
dotnet sln add folder/myapp.csproj
```

> Use an array of projects to add multiple

`dotnet sln add [project]`

```
dotnet sln add folder1/myapp1.csproj folder2/myapp2.csproj
```

## Nuget Packages

### Restore

Restores packages to the solution.  Downloads and installs dependent code required for the solution and projects to run

> This command can be run for the solution or for each individual project in the solution

`dotnet restore`

```
dotnet restore
```

### List Nuget Packages

Lists the referenced nuget packages for the solution and projects

`dotnet list package`

```
dotnet list package
```

### Add Package

Adds a new nuget package to project file.  By default this will install the latest version available

`dotnet add package <package>`

```
dotnet add package Newtonsoft.Json
```

> To install a specific version add the --version parameter

`dotnet add package <package> --version <version>`

```
dotnet add package Newtonsoft.Json --version 12.0.1
```

### Remove Package

Removes the specified package from the project file

`dotnet remove package <package>`

```
dotnet remove package Newtonsoft.Json
```

## Build

Builds the solution and all project files

> This command can be run at both the solution level and project level.  If run at the solution it will build all projects in the solution.

`dotnet build [args]`

```
dotnet build
```

## Run

Runs the solution and every project or just the specified project

> This command can be run at both the solution level and project level.  If run at the solution it will build all projects in the solution.

`dotnet run [args]`

```
dotnet run
```

## Test

Run all test project types within the solution

> This command can be run at both the solution level and project level.  If run at the solution it will build all projects in the solution.

`dotnet test [args]`

```
dotnet test
```

> To collect code coverage

```
dotnet test --collect "Code Coverage"
```

> To use a runsettings file

```
dotnet test --settings=.runsettings
```

## Publish

Packages code for deployment

`dotnet publish [args]`

```
dotnet publish
```

> Publish out to a specific directory or path

`dotnet publish -o <path>`

```
dotnet publish -o ./bin/publish
```

> Publish for a specific framework and runtime

`dotnet publish --framework <framework> --runtime <runtime>`

```
dotnet publish --framework .net6.0 --runtime osx.10.11-x64
```