# Security Policy

## Supported Versions

We provide security updates for the following versions of PandocTool:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| < Latest| :x:                |

We recommend always using the latest version of PandocTool to ensure you have the latest security updates.

## Reporting a Vulnerability

If you discover a security vulnerability in PandocTool, please report it responsibly:

### Do Not

* Open a public GitHub issue for security vulnerabilities
* Disclose the vulnerability publicly before it has been addressed

### Please Do

1. Email details of the vulnerability to [security@demaconsulting.com][email]
2. Include the following information:
   * Type of vulnerability
   * Affected versions
   * Steps to reproduce
   * Potential impact
   * Any suggested fixes (if available)

### What to Expect

* **Initial Response**: You will receive an acknowledgment within 48 hours
* **Assessment**: We will assess the vulnerability and determine its severity
* **Fix Development**: We will work on a fix and may contact you for additional information
* **Release**: Once fixed, we will release a new version and credit you for the discovery (unless you prefer to remain anonymous)
* **Disclosure**: We aim to disclose vulnerabilities responsibly after a fix is available

## Security Best Practices

When using PandocTool:

* Always use the latest version
* Keep your .NET runtime up to date
* Review the [release notes][releases] for security updates
* Follow security best practices for your development environment

## Dependencies

PandocTool packages the Pandoc universal document converter. Security issues in Pandoc itself should be
reported to the [Pandoc project][pandoc-security].

## Scope

This security policy applies to:

* The PandocTool dotnet tool wrapper
* The packaging and distribution process
* Build and deployment workflows

This policy does not cover:

* Security issues in Pandoc itself (report to Pandoc project)
* Security issues in third-party dependencies (report to respective projects)
* Security issues in user-generated documents

## Recognition

We appreciate security researchers who follow responsible disclosure practices.
Contributors who report valid security vulnerabilities will be acknowledged in the release notes
(unless they prefer to remain anonymous).

[email]: mailto:security@demaconsulting.com
[releases]: https://github.com/demaconsulting/PandocTool/releases
[pandoc-security]: https://github.com/jgm/pandoc/security
