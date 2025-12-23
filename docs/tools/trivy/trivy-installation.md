# Trivy

## Installation

As docker image:
```
docker pull aquasec/trivy
```

## Usage

Scan a docker image:
```
docker run --rm -it aquasec/trivy image <docker_image>
```

Scan a docker image for secrets only:
```
docker run --rm -it aquasec/trivy image --scanners secret <docker_image>
```

Scan a local repository (in current folder):

On Windows:
```
docker run --rm -it -v "%cd%:/src" aquasec/trivy fs /src
```

### Options

Output file format:
```
JSON: -f json
SARIF: -f sarif
```

Output file:
```
-o <output_file>
```

## References

1. [Trivy](https://trivy.dev/latest/)
1. [Trivy GitHub](https://github.com/aquasecurity/trivy)

***
*Updated on 23 December 2025*
