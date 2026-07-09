# Windows Subsystem for Linux (WSL)

## Reference

1. [How to install Linux on Windows with WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
1. [Install Multiple Copies of Ubuntu in Windows WSL](https://www.maketimelabs.com/installing-multiple-copies-of-ubuntu-in-windows-wsl/)
1. [Python setup on the Windows subsystem for Linux (WSL)](https://medium.com/@rhdzmota/python-development-on-the-windows-subsystem-for-linux-wsl-17a0fa1839d)

## Installation of WSL

### Enable WSL

To enable the features necessary to run WSL and install the Ubuntu distribution of Linux. (This default distribution can be changed.)
```
C:> wsl --install
```

### Update Ubuntu Packages

```
$ sudo apt update
$ sudo apt list --upgradable
$ sudo apt upgrade
```

### Install Python and virtualenv For Ubuntu on WSL

```
$ sudo apt install python3 python3-pip
$ sudo pip3 install virtualenv
```

### Starting and Stopping WSL

Starting WSL
```
C:> wsl
```

Stopping WSL
```
$ exit
```

### Update WSL

```
C:> wsl --update --web-download
```

***
***

## Install a Second Copy of Ubuntu on WSL

### Installation Steps

1. Download the Ubuntu images for WSL from [here](https://releases.ubuntu.com/noble/).
1. Install the downloaded images.
    ```
    wsl --install --from-file <Downloaded *.wsl File> --name <Distribution Name> --no-launch
    ```
1. Check that <Distribution Name> is properly imported.
    ```
    wsl -l -v
    ```
1. Start new instance using
    ```
    wsl -d <Distribution Name>
    ```

### Unregister or Uninstall a Linux Distribution

```
wsl --unregister <Distribution Name>
```

***
*Updated on 9 July 2026*
