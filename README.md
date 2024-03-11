![GitHub forks](https://img.shields.io/github/forks/demaconsulting/PandocTool?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/demaconsulting/PandocTool?style=plastic)
![GitHub contributors](https://img.shields.io/github/contributors/demaconsulting/PandocTool?style=plastic)
![GitHub](https://img.shields.io/github/license/demaconsulting/PandocTool?style=plastic)

# About

PandocTool is the [Pandoc](https://pandoc.org/) universal document converter packaged as a Dotnet tool.

Pandoc is already available in numerous formats for [installation](https://pandoc.org/installing.html).
Packaging it as a Dotnet tool allows for multiple versions to be installed and cached on a system
simultaneously, and users can control which version is used through a
[Dotnet tool manifest file](https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools#install-a-local-tool).


# Installation & Usage

The following will add PandocTool to a Dotnet tool manifest file:

```
dotnet new tool-manifest # if you are setting up this repo
dotnet tool install --local DEMAConsulting.PandocTool
```

The tool can then be executed by:

```
dotnet pandoc <arguments>
```
