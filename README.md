# PandocTool

[![NuGet Version][nuget-badge]][nuget-link]
[![GitHub Forks][forks-badge]][repo-link]
[![GitHub Stars][stars-badge]][repo-link]
[![GitHub Contributors][contributors-badge]][repo-link]
[![GitHub License][license-badge]][repo-link]

## About

PandocTool is a repackaging of the [Pandoc][pandoc-home] Universal Document Converter as a
[.NET tool][dotnet-tools-docs].

Pandoc is already available in numerous formats for [installation][pandoc-install].
Packaging it as a .NET tool allows for multiple versions to be installed and cached on a system
simultaneously, and users can control which version is used through a
[.NET tool manifest file][dotnet-manifest-docs].

## Installation & Usage

The following will add PandocTool to a .NET tool manifest file:

```bash
dotnet new tool-manifest # if you are setting up this repo
dotnet tool install --local DEMAConsulting.PandocTool
```

The tool can then be executed by:

```bash
dotnet pandoc <arguments>
```

## Contributing

Contributions are welcome! Please see our [Contributing Guidelines][contributing] for details.

## Code of Conduct

This project has adopted the [Contributor Covenant Code of Conduct][code-of-conduct].

## Security

For security issues, please see our [Security Policy][security].

## License

This project is licensed under the GPL-2.0-or-later license. See the [LICENSE][license] file for details.

[nuget-badge]: https://img.shields.io/nuget/v/DEMAConsulting.PandocTool?style=plastic
[nuget-link]: https://www.nuget.org/packages/DEMAConsulting.PandocTool
[forks-badge]: https://img.shields.io/github/forks/demaconsulting/PandocTool?style=plastic
[stars-badge]: https://img.shields.io/github/stars/demaconsulting/PandocTool?style=plastic
[contributors-badge]: https://img.shields.io/github/contributors/demaconsulting/PandocTool?style=plastic
[license-badge]: https://img.shields.io/github/license/demaconsulting/PandocTool?style=plastic
[repo-link]: https://github.com/demaconsulting/PandocTool
[pandoc-home]: https://pandoc.org/
[pandoc-install]: https://pandoc.org/installing.html
[dotnet-tools-docs]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools
[dotnet-manifest-docs]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools#install-a-local-tool
[contributing]: https://github.com/demaconsulting/PandocTool/blob/main/CONTRIBUTING.md
[code-of-conduct]: https://github.com/demaconsulting/PandocTool/blob/main/CODE_OF_CONDUCT.md
[security]: https://github.com/demaconsulting/PandocTool/blob/main/SECURITY.md
[license]: https://github.com/demaconsulting/PandocTool/blob/main/LICENSE
