# Security Tools Installation Guide

## JWT Tools

1. The JSON Web Token Toolkit v2

    Clone from GitHub:
    ```
    git clone https://github.com/ticarpi/jwt_tool.git
    ```

    For Linux and Windows:
    ```
    python3 -m pip install termcolor cprint pycryptodomex requests
    ```

    Additional Steps for Windows:
    ```
    python3 -m pip install colorama
    ```
    and uncomment the two lines in jwt_tool.py:
    ```
    # import colorama
    # colorama.init()
    ```

    For Python virtual environment, create python virtualenv named tools
    ```
    (tools) $ python3 -m pip install termcolor cprint pycryptodomex requests
    (tools) $ cd jwt_tool
    (tools) $ chmod u+x jwt_tool.py
    ```

***
*Updated on 3 February 2026*
