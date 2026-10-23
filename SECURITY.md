# Security Policy

## Supported Versions

This repository is a security engineering portfolio project and does not publish
versioned releases. Security fixes are applied to the `main` branch only.

| Branch | Supported          |
| ------ | ------------------ |
| main   | :white_check_mark: |

## Reporting a Vulnerability

**Please do not open a public issue, pull request, or discussion for a security
vulnerability.**

Report privately using GitHub's **Private vulnerability reporting**:

1. Go to the **Security** tab of this repository.
2. Click **Report a vulnerability**.
3. Describe the issue with reproduction steps, impact, and affected files.

If private reporting is unavailable, contact the maintainer directly through the
contact method listed on the [maintainer's GitHub profile](https://github.com/snrtech-del).

### What to include

- A clear description of the issue and its security impact
- Steps to reproduce (proof-of-concept preferred)
- Affected file paths, workflow names, or commit SHAs
- Any suggested remediation
- Whether you intend to disclose publicly, and on what timeline

### What to expect

| Stage | Target |
| ----- | ------ |
| Acknowledgement of report | 3 business days |
| Initial assessment / triage | 7 business days |
| Status update cadence | Every 7 days until resolved |
| Fix or documented mitigation | 30 days for High/Critical, best effort otherwise |

If a report is **accepted**, you will receive credit in the advisory unless you
request otherwise. If a report is **declined**, you will receive a written
explanation of why it falls outside scope or does not constitute a vulnerability.

### Coordinated disclosure

Please allow up to **90 days** from acknowledgement before public disclosure, or
until a fix is released — whichever comes first. We will coordinate a disclosure
date with you and publish a GitHub Security Advisory.

## Scope

**In scope:**

- GitHub Actions workflow definitions in `.github/workflows/`
- Vulnerabilities in pipeline configuration that could lead to secret exposure,
  arbitrary code execution, or supply-chain compromise
- Insecure defaults in scanner configuration files
- Scripts and tooling committed to this repository
- Documentation that could mislead users into an insecure configuration

**Out of scope:**

- Vulnerabilities in third-party tools, actions, or scanners themselves — report
  those upstream to the respective project
- Findings that require a compromised maintainer account or GitHub platform access
- Missing hardening controls that are already tracked as open issues
- Reports generated solely by an automated scanner without demonstrated impact
- Social engineering, physical access, or denial-of-service against GitHub itself

## Security practices in this repository

- All third-party GitHub Actions are pinned to full commit SHAs
- `GITHUB_TOKEN` defaults to read-only; write permissions are granted per job
- Secret scanning with push protection is enabled
- CodeQL code scanning runs on every push and pull request to `main`
- Dependabot alerts and security updates are enabled
- The `main` branch requires pull requests, passing status checks, and signed commits

## Safe harbor

We will not pursue legal action against researchers who act in good faith,
follow this policy, avoid privacy violations and service disruption, and give
reasonable time to remediate before disclosure.
