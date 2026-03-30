# Audit for Secrets in Code

**Audit your own code for accidentally committed secrets**: Use dedicated tools like git-secrets, truffleHog, or detect-secrets

# Secret Scanning Tools

1. [TruffleHog](https://trufflesecurity.com/trufflehog)
1. [Gitleaks](https://gitleaks.io/)
1. [Snyk AI Security Platform](https://snyk.io/)

***
***

# Installation

## Gitleaks

Installation on Docker from DockerHub:
```bash
# Docker (DockerHub)
docker pull zricethezav/gitleaks:latest
```

Alternative - Installation on Docker from ghcr.io:
```bash
# Docker (ghcr.io)
docker pull ghcr.io/gitleaks/gitleaks:latest
```

Usage:
```bash
docker run --rm -v ${path_to_host_folder_to_scan}:/path zricethezav/gitleaks:latest [COMMAND] [OPTIONS] [SOURCE_PATH]
```

Check Version:
```bash
docker run --rm zricethezav/gitleaks:latest version
```

Scan Current Directory:
```bash
docker run --rm -v .:/path zricethezav/gitleaks:latest dir /path
```

Scan Current Directory and Write Results to a file:
```bash
docker run --rm -v .:/path zricethezav/gitleaks:latest dir --report-path /path/findings.json /path
```

***
*Updates on 30 March 2026*
