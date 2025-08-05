# Semgrep Installation

## References

1. [Semgrep](https://semgrep.dev/)
1. [Semgrep Quickstart](https://semgrep.dev/docs/getting-started/)

## Installing Semgrep on Python

### Preparation

Set up Windows Subsystem for Linux (WSL) for Windows. This step is for Windows only.

1. On Windows, Semgrep needs to be installed in Windows Subsystem for Linux (WSL).
    - See [here](../../os/windows/windows-wsl-installation.md) on how to enable WSL.
1. Semgrep cannot be installed directly on Windows.

Set up a virtual environment if necessary.

1. A Python virtual environment could be set up for running semgrep.
    - Use your favourite Python virtual environment or see [here](../../language/python/python-virtualenv-windows.md) for instruction on how to set up one.

### Installation of Semgrep on Python

1. Assume that semgrep is the name of the virtual environment, install Semgrep using pip.
    ```
    (semgrep) $ pip install semgrep
    ```
1. Check that Semgrep is properly installed.
    ```
    (semgrep) $ semgrep --version
    ```

### Using Semgrep on Python

```
(semgrep) $ semgrep --config=auto <PATH/TO/SRC>
(semgrep) $ semgrep --config=<PATH/TO/RULES> <PATH/TO/SRC>
```

### Obtaining the Community Rules

Reference: [Semgrep Community Rules](https://github.com/returntocorp/semgrep-rules)
```
$ git clone https://github.com/returntocorp/semgrep-rules.git
```

### Using Semgrep in CI Jobs

Reference: [Add Semgrep to CI](https://semgrep.dev/docs/semgrep-ci/overview/)

***
***

## Using Semgrep on Docker

Update: Semgrep Docker image is now at semgrep/semgrep.

Getting the Docker image for Semgrep
```
$ docker pull returntocorp/semgrep
```

Test the Docker image for Semgrep
```
$ docker run --rm returntocorp/semgrep semgrep --version
```

Run with recommended semgrep rules, on the source in the current directory.

1. On Linux/MacOS
    ```
    $ docker run --rm -v "${PWD}:/src" returntocorp/semgrep semgrep --config=auto
    ```
1. On Windows
    ```
    $ docker run --rm -v "%CD%:/src" returntocorp/semgrep semgrep --config=auto
    ```

Run with local rules.

```
$ docker run --rm -v "${PWD}:/src" -v "${PWD}/../../git-clone/semgrep-rules:/rules" returntocorp/semgrep semgrep --config=/rules
```

***
***

## Sample Projects for Testing Semgrep

Reference: [Semgrep Quickstart](https://semgrep.dev/docs/getting-started/)

1. juice-shop, a vulnerable Node.js + Express app:
    ```
    git clone https://github.com/bkimminich/juice-shop
    cd juice-shop
    semgrep --config=auto
    ```

    Or if you don't have Semgrep installed, replace the semgrep command with:
    ```
    docker run --rm -v "$(pwd)/juice-shop:/src" returntocorp/semgrep semgrep --config p/security-audit /src
    ```

1. railsgoat, a vulnerable Ruby on Rails app:
    ```
    git clone https://github.com/OWASP/railsgoat
    cd railsgoat
    semgrep --config=auto
    ```

1. govwa, a vulnerable Go app:
    ```
    git clone https://github.com/0c34/govwa
    cd govwa
    semgrep --config=auto
    ```

1. Vulnerable-Flask-App, vulnerable Python + Flask:
    ```
    git clone https://github.com/we45/Vulnerable-Flask-App
    cd Vulnerable-Flask-App
    semgrep --config=auto
    ```

1. WebGoat, a vulnerable Java + Spring app:
    ```
    git clone https://github.com/WebGoat/WebGoat
    cd WebGoat
    semgrep --config=auto
    ```
### List of Known Vulnerabilities

1. [juice-shop](https://grietsdc.in/downloads/nasscom161121/pwning%20-%20JuiceShop.pdf)

***
*Updated on 5 Auguest 2025*
