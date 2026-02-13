# Python UV Installation Guide

## Reference

1. [Managing Python Virtual Environments with UV: A Comprehensive Guide](https://medium.com/@vkmauryavk/managing-python-virtual-environments-with-uv-a-comprehensive-guide-ac74d3ad8dff)
1. [Using Python Environments](https://docs.astral.sh/uv/pip/environments/)

## Installation of uv

Install uv in the main Python environment using pip:
```bash
pip install uv
```

Verification:
```bash
uv --version
```

## Create and Manage Virtual Environments Using uv

1. Create a virtual environment in the .venv directory
    ```bash
    uv venv
    ```

    Specify a Python version:
    ```bash
    uv venv --python 3.11
    ```

1. Activating the Virtual Environment
    ```bash
    source .venv/bin/activate   # for Linux/Mac
    .venv\Scripts\activate.bat  # for Windows
    ```

1. Installing Dependencies
    Install Packages
    ```bash
    (venv) $ uv pip install requests
    ```

    Add dependencies to the ```pyproject.toml``` file
    ```bash
    (venv) $ uv add requests
    ```

    To generate ```pyproject.toml``` file use the following. It will create a few files.
    ```bash
    (venv) $ uv init
    ```

1. Deactivating the virtual environment
    ```bash
    (venv) $ deactivate
    ```

***
*Updated on 13 February 2026*
