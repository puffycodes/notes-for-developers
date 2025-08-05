# Semgrep CLI Token

## Reference

1. [Semgrep CLI](https://semgrep.dev/onboarding/scan)

## Installation

Install semgrep pro:
```
semgrep install-semgrep-pro
```

## Token

Run the following command to log in to the Semgrep CLI.

On Mac,
```
SEMGREP_APP_TOKEN=<token_value> semgrep login
```

On Linux,
```
SEMGREP_APP_TOKEN=<token_value> semgrep login
```

Using Docker on Mac or Linux,
```
docker run -e SEMGREP_APP_TOKEN=<token_value> --rm -v "${PWD}:/src" semgrep/semgrep semgrep ci
```

Using Docker, On Windows,
```
docker run -e SEMGREP_APP_TOKEN=<token_value> --rm -v "%cd%:/src" semgrep/semgrep semgrep ci
```

***
*Updated on 5 August 2025*
