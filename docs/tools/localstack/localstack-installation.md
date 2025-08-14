# LocalStack

## References

1. [LocalStack](https://www.localstack.cloud)
1. [Installation](https://docs.localstack.cloud/aws/getting-started/installation)
1. [Quick Start](https://docs.localstack.cloud/aws/getting-started/quickstart)

## Installation

1. Pre-requisite: Need a working installation of Docker.

1. Install LocalStack CLI for Python with Pip.

    ```
    python -m pip install --upgrade localstack
    ```
    - If you have problems with permissions in MacOS X Sierra, install with:
        ```
        python -m pip install --user localstack
        ```
    - Do not use sudo or root user when starting LocalStack. It should be installed and started entirely under a local non-root user.
    - On Windows, may need to [enable long paths](#enabling-windows-long-paths) if pip gives warning.

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

## Other methods of starting LocalStack

### Using Docker

For Community Edition:
```
docker run \
  --rm -it \
  -p 127.0.0.1:4566:4566 \
  -p 127.0.0.1:4510-4559:4510-4559 \
  -v /var/run/docker.sock:/var/run/docker.sock \
  localstack/localstack
```

For Pro Edition:
```
docker run \
  --rm -it \
  -p 127.0.0.1:4566:4566 \
  -p 127.0.0.1:4510-4559:4510-4559 \
  -p 127.0.0.1:443:443 \
  -e LOCALSTACK_AUTH_TOKEN=${LOCALSTACK_AUTH_TOKEN:?} \
  -v /var/run/docker.sock:/var/run/docker.sock \
  localstack/localstack-pro
```

## Enabling Windows Long Paths

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
