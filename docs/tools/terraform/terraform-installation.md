# Terraform Installation Guide

## References

1. [Terraform Home Page](https://www.terraform.io/)

## Installation

### For MacOS

Install Terraform Using Homebrew:
```
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

Note: May need to do this to install the command line developer tools:
```
xcode-select --install
```

Upgrade:
```
brew update hashicorp/tap/terraform
```

### For Windows

1. Download Windows Binary (386 or AMD64).
1. Copy the file terraform.exe into a directory in the system path.
    1. Alternatively, add the folder that the file is in to the system path.

### Test Run

```
terraform version
```

***
*Updated on 14 August 2025*
