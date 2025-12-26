# Contributing to PandocTool

Thank you for your interest in contributing to PandocTool! We welcome contributions from the community.

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct][code-of-conduct].
By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates.
When you create a bug report, include as many details as possible:

* Use the bug report template
* Provide a clear and descriptive title
* Describe the exact steps to reproduce the problem
* Provide specific examples to demonstrate the steps
* Describe the behavior you observed and what behavior you expected to see
* Include your PandocTool version, .NET version, and operating system

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

* Use the feature request template
* Provide a clear and descriptive title
* Provide a detailed description of the suggested enhancement
* Explain why this enhancement would be useful
* List any alternative solutions you've considered

### Pull Requests

* Fill in the required template
* Follow the coding style used in the project
* Include appropriate test coverage for your changes
* Update documentation as needed
* Ensure all tests pass before submitting
* Run spelling and markdown linting checks and fix any issues

## Development Guidelines

### Setting Up Your Development Environment

1. Fork and clone the repository
2. Ensure you have .NET 8.0 or later installed
3. Restore the dotnet tools: `dotnet tool restore`

### Building the Project

The project uses a build workflow that downloads Pandoc binaries and packages them as a dotnet tool:

```bash
# The build process is primarily handled through GitHub Actions
# Local testing can be done by examining the .github/workflows/build.yaml file
```

### Coding Standards

* Follow standard C# coding conventions
* Use meaningful variable and method names
* Add comments for complex logic
* Keep methods focused and concise

### Documentation Standards

* All markdown files must use absolute URLs (not relative URLs) for links
* This is required because the README.md is distributed in the NuGet package
* Use markdown link reference format for all links
* Follow markdown linting rules defined in .markdownlint.json
* Follow spelling rules defined in .cspell.json

### Testing Your Changes

Before submitting a pull request:

1. Build the project to ensure it compiles
2. Run all existing tests
3. Add tests for new functionality
4. Run spelling checks: `npx cspell "**/*.md" "**/*.yaml" "**/*.yml" "**/*.json"`
5. Run markdown linting: `npx markdownlint-cli "**/*.md"`
6. Verify that your changes work as expected

### Commit Messages

* Use clear and meaningful commit messages
* Start with a verb in the present tense (e.g., "Add", "Fix", "Update")
* Keep the first line under 72 characters
* Add detailed description if needed in the commit body

### Pull Request Process

1. Update the README.md or other documentation with details of changes if applicable
2. Ensure all tests pass and code follows the project's style guidelines
3. Run quality checks (spelling and markdown linting)
4. The pull request will be reviewed by maintainers
5. Address any feedback or requested changes
6. Once approved, your pull request will be merged

## Recognition

Contributors will be recognized in the project's release notes and commit history.

## Questions?

Feel free to open a discussion on GitHub if you have questions about contributing.

## License

By contributing to PandocTool, you agree that your contributions will be licensed
under the GPL-2.0-or-later license.

[code-of-conduct]: https://github.com/demaconsulting/PandocTool/blob/main/CODE_OF_CONDUCT.md
