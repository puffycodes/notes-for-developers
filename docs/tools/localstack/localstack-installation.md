# LocalStack

## References

1. [LocalStack](https://www.localstack.cloud)

## Installation

Reference: [Installation](https://docs.localstack.cloud/aws/getting-started/installation)

1. Need a working installation of Docker.
1. Install LocalStack CLI for Python with Pip.

    ```
    python -m pip install --upgrade localstack
    ```
    - If you have problems with permissions in MacOS X Sierra, install with:
        ```
        python -m pip install --user localstack
        ```
    - Do not use sudo or root user when starting LocalStack. It should be installed and started entirely under a local non-root user.
    - On Windows, may need to [enable long path](#enabling-windows-long-path) if pip gives warning.
1. Verify LocalStack
    ```
    localstack --version
    ```
1. Start LocalStack
    ```
    localstack start
    ```
    1. Start LocalStack in backgroun with -d flag.
    1. Pull docker image first, if necessary.

        For Community Edition:
        ```
        docker pull localstack/localstack
        ```

        For Pro Edition:
        ```
        docker pull localstack/localstack-pro
        ```
1. Update LocalStack
    ```
    localstack update --help
    ```

## Enabling Windows Long Path

1. [Reference 1](https://pip.pypa.io/warnings/enable-long-paths)
1. [Reference 2](https://learn.microsoft.com/en-us/windows/win32/fileio/maximum-file-path-limitation?tabs=registry#enable-long-paths-in-windows-10-version-1607-and-later)
1. Use the following .reg file:
    ```
    Windows Registry Editor Version 5.00

    [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
    "LongPathsEnabled"=dword:00000001
    ```

***
*Updated on 13 August 2025*
