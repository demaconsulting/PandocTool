# Agent Instructions for PandocTool

This document provides instructions for AI agents (such as GitHub Copilot) working on the PandocTool repository.

## Project Overview

PandocTool is a dotnet tool wrapper for [Pandoc][pandoc], the universal document converter.
The project packages Pandoc binaries for Windows and Linux platforms as a dotnet tool,
allowing multiple versions to be installed and managed via dotnet tool manifests.

## Key Project Constraints

### README.md Link Requirements

**CRITICAL**: The README.md file must only contain absolute URLs, not relative URLs.

* **Reason**: The README.md file is distributed in the NuGet package and will be displayed on NuGet.org
* **Requirement**: All links in README.md must be absolute URLs (e.g., `https://github.com/...`)
* **Format**: Use markdown link reference format for all links
* **Validation**: Verify all links are absolute before committing changes

### Link Reference Format

All markdown files should use the link reference format for better maintainability:

```markdown
Example: [link text][reference-id]

[reference-id]: https://full.url/path
```

## Code Quality Standards

### Spelling Checks

* Run spelling checks before committing: `npx cspell "**/*.md" "**/*.yaml" "**/*.yml" "**/*.json"`
* Add new technical terms to the `.cspell.json` words list if needed
* Ensure all markdown, YAML, and JSON files pass spelling checks
* **Required**: All changes must pass spelling checks

### Markdown Linting

* Run markdown linting before committing: `npx markdownlint-cli "**/*.md"`
* Follow the rules defined in `.markdownlint.json`
* Fix any linting errors before submitting changes
* **Required**: All changes must pass markdown linting

## Testing Changes

Before considering work complete:

1. **Spelling Check**: Run `npx cspell "**/*.md" "**/*.yaml" "**/*.yml" "**/*.json"`
2. **Markdown Linting**: Run `npx markdownlint-cli "**/*.md"`
3. **Build Verification**: Ensure the project builds successfully (if code changes were made)
4. **Workflow Validation**: Verify GitHub Actions workflows are valid YAML

## Project Structure

* `/pack/` - Contains the NuGet package definition and tool wrappers
* `/.github/workflows/` - GitHub Actions workflows for build and release
* `/README.md` - Main documentation (must use absolute URLs)
* `/CODE_OF_CONDUCT.md` - Community code of conduct
* `/CONTRIBUTING.md` - Contribution guidelines
* `/SECURITY.md` - Security policy
* `/AGENTS.md` - This file, instructions for AI agents

## Build Process

The project uses GitHub Actions to:

1. Download the DotnetToolWrapper from releases
2. Download Pandoc binaries for Windows (x64) and Linux (x64)
3. Package everything as a dotnet tool
4. Generate SBOM (Software Bill of Materials)
5. Create a NuGet package
6. Test the package on Windows and Linux with .NET 8, 9, and 10

Local builds are not typically performed; the CI/CD pipeline handles packaging.

## CI Testing

The build workflow includes automated testing:

* **Build Job**: Runs on ubuntu-latest to create the NuGet package
* **Test Job**: Matrix tests the package on:
  * Operating Systems: Windows and Linux
  * .NET Versions: 8, 9, and 10
  * Tests verify the packaged pandoc tool executes correctly by running `pandoc --version` and `pandoc --help`

## Documentation Standards

* Use clear, concise language
* Provide examples where helpful
* Keep documentation up to date with code changes
* Follow markdown formatting standards
* Use absolute URLs in README.md
* Use link reference format for all links

## Common Tasks

### Updating Dependencies

Dependencies are managed through:

* GitHub Actions versions in workflow files
* Dotnet tools in `.config/dotnet-tools.json`
* Dependabot configuration in `.github/dependabot.yml`

### Adding New Features

1. Review CONTRIBUTING.md for guidelines
2. Ensure changes maintain compatibility
3. Update documentation as needed
4. Add tests if applicable
5. Run quality checks (spelling and markdown linting)

### Making Documentation Changes

1. Edit the relevant markdown file
2. Ensure README.md links are absolute URLs
3. Use link reference format
4. Run spelling checks
5. Run markdown linting
6. Verify formatting is correct

## Important Notes

* **README.md URLs**: Always use absolute URLs in README.md (distributed with NuGet package)
* **Quality Checks**: Always run spelling and markdown linting checks before completing work
* **Link Format**: Use markdown link reference format for maintainability
* **Compatibility**: Maintain compatibility with supported .NET versions (8, 9, 10)
* **License**: Project uses GPL-2.0-or-later license

## Resources

* [Pandoc Documentation][pandoc-docs]
* [Dotnet Tools Documentation][dotnet-tools]
* [GitHub Actions Documentation][github-actions]
* [Markdown Guide][markdown-guide]

[pandoc]: https://pandoc.org/
[pandoc-docs]: https://pandoc.org/
[dotnet-tools]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools
[github-actions]: https://docs.github.com/en/actions
[markdown-guide]: https://www.markdownguide.org/
