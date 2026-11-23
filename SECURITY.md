# Security policy

## Supported versions

Security fixes land on the default branch (`main`) of active repositories. Archived repositories (`[SUPERSEDED BY ...]`) remain read-only historical records and do not receive patches.

## Reporting a vulnerability

Do not open a public GitHub issue for suspected security flaws, credential leaks, SSRF bypasses, or authentication bugs.

1. Open the target repository `Security` tab and file a report through `Report a vulnerability` (GitHub Private Vulnerability Reporting): `https://github.com/<owner>/<repo>/security/advisories/new`.
2. If Private Vulnerability Reporting is inactive on that repository, email the Abstrekkt Security Desk at `Kyle@abstrekkt.com` with the repository name, commit SHA, and minimal reproduction steps.
3. Include affected file paths and proof-of-concept steps without posting live secret values in plaintext comments.

## Baseline engineering controls

- Never commit `.env` files, API credentials, service-account JSON files, or bearer tokens.
- Pin GitHub Actions `uses:` steps to 40-character commit SHAs and set top-level `permissions: contents: read` by default.
- Validate outbound webhook and MCP URLs against private and reserved CIDR ranges before network calls.
