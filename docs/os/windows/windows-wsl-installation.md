# Windows Subsystem for Linux (WSL)

Reference:

1. [How to install Linux on Windows with WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
1. [Python setup on the Windows subsystem for Linux (WSL)](https://medium.com/@rhdzmota/python-development-on-the-windows-subsystem-for-linux-wsl-17a0fa1839d)

## Installation of WSL

To enable the features necessary to run WSL and install the Ubuntu distribution of Linux. (This default distribution can be changed.)
```
C:> wsl --install
```

## Update Ubuntu Packages

```
$ sudo apt update
$ sudo apt list --upgradable
$ sudo apt upgrade
```

## Install Python and virtualenv For Ubuntu on WSL

```
$ sudo apt install python3 python3-pip
$ sudo pip3 install virtualenv
```

## Starting and Stopping WSL

Starting WSL
```
C:> wsl
```

Stopping WSL
```
$ exit
```

***
*Updated on 4 August 2025*
