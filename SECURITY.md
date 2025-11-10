# Security Policy

## Supported Versions

This project is actively maintained. Security updates will be applied to the latest version.

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please help us keep the project safe by reporting it responsibly.

**Please do not create public GitHub issues for security vulnerabilities.**

Instead, please email me directly at [andreagriffiths11@gmail.com] with:

- A description of the vulnerability
- Steps to reproduce the issue
- Potential impact
- Any suggested fixes (if you have them)

I'll respond within 48 hours and work with you to understand and address the issue.

## Security Considerations

This tool generates bash scripts that modify git repositories. Users should:

- Always create backups before running generated scripts
- Review and understand each command before execution
- Never run scripts on production repositories without proper testing
- Be cautious when sharing or storing generated scripts as they may contain repository names

## Scope

Since this is a client-side web application that generates scripts locally, the main security concerns are:

- Cross-site scripting (XSS) prevention
- Input sanitization for repository names
- Safe script generation practices

Thank you for helping keep this project secure!
