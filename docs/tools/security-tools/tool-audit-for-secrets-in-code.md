# Audit for Secrets in Code

**Audit your own code for accidentally committed secrets**: Use dedicated tools like git-secrets, truffleHog, or detect-secrets

# Contents

1. [Secret Scanning Tools](#secret-scanning-tools)
1. [Installation](#installation)
    1. [TruffleHog](#trufflehog)
    1. [GitLeaks](#gitleaks)

# Secret Scanning Tools

1. [TruffleHog](https://trufflesecurity.com/trufflehog)
1. [Gitleaks](https://gitleaks.io/)
1. [gitsecrets](https://github.com/awslabs/git-secrets)
1. [detect-secrets](https://github.com/Yelp/detect-secrets)
1. [Snyk AI Security Platform](https://snyk.io/)

***
***

# Installation

## TruffleHog

Installation on Docker:
```bash
docker pull trufflesecurity/trufflehog:latest
```

Usage (Unix):
```bash
docker run --rm -it -v "$PWD:/pwd" trufflesecurity/trufflehog:latest github --repo https://github.com/trufflesecurity/test_keys
```

Usage (Windows):
```cmd
docker run --rm -it -v "%cd:/=\%:/pwd" trufflesecurity/trufflehog:latest github --repo https://github.com/trufflesecurity/test_keys
```

Usage (PowerShell):
```
docker run --rm -it -v "${PWD}:/pwd" trufflesecurity/trufflehog github --repo https://github.com/trufflesecurity/test_keys
```

Usage (M1 and M2 Mac):
```bash
docker run --platform linux/arm64 --rm -it -v "$PWD:/pwd" trufflesecurity/trufflehog:latest github --repo https://github.com/trufflesecurity/test_keys
```

Scan Current Directory:
```bash
docker run --rm -it -v .:/pwd trufflesecurity/trufflehog:latest filesystem /pwd
```

***
***

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
*Updates on 31 March 2026*
