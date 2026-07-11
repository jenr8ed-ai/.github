# Security Policy

## Supported Versions

Active development. Report issues against the latest main.

## Reporting a Vulnerability

**Please do not open public issues for security vulnerabilities.**

Email: jen.mckinley@gmail.com with subject "SECURITY: <short description>"

Include:
- Description of the vulnerability
- Steps to reproduce / proof of concept
- Potential impact (especially regarding credential exposure or FSAD data integrity)
- Suggested fix if known

We aim to respond within 48 hours for high-severity reports.

## Scope

- Any accidental secret or token committed to a JenR8ed repo (violates zero-credential policy)
- Weaknesses in publishing automation, FSAD syncs, or dashboards that could leak private relations data
- Agent workflow issues that could lead to unintended data exposure or publication of sensitive content
- Infrastructure (Cloudflare Pages, Apps Script, Docker, n8n, etc.)

## Hall of Thanks

Responsible disclosures will be acknowledged (unless anonymity requested).

## Related

See also [dash-governance.md](https://github.com/JenR8ed/.github/blob/main/docs/governance/dash-governance.md) and the zero-token rules in the SOT.