# Security Policy

## Supported Versions

| Version | Supported |
|---|---|
| 2.4.x (latest) | :white_check_mark: |
| 2.3.x | :white_check_mark: |
| < 2.3 | :x: |

## Reporting a Vulnerability

If you discover a security vulnerability in Vanguard, please report it responsibly.

**DO NOT** open a public GitHub issue for security vulnerabilities.

Instead, please report via one of these channels:

1. **GitHub Security Advisories**: Use [GitHub's private vulnerability reporting](https://github.com/hadionlineclas/vanguard/security/advisories/new)
2. **Direct Contact**: Reach out to **hadionlineclas** on GitHub

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

### Response Timeline

- **Acknowledgment**: Within 48 hours
- **Initial Assessment**: Within 1 week
- **Fix/Patch**: Depending on severity, typically within 2 weeks

## Security Considerations

Vanguard is designed with security in mind:

- **Local-first**: Vanguard runs entirely on your machine. Your code never passes through our servers.
- **API keys**: Stored locally in your config or environment variables. Never transmitted to Vanguard infrastructure.
- **No telemetry**: Zero data collection. No analytics, no tracking, no phone-home.
- **Open source**: Every line of code is auditable. Security through transparency.

## Best Practices for Users

- Keep Vanguard updated to the latest version
- Use environment variables (`env:VAR_NAME`) for API keys instead of hardcoding them
- Review the `vanguard.config.json` before committing — ensure no API keys are included
- Add `vanguard.config.json` to `.gitignore` if it contains sensitive values
