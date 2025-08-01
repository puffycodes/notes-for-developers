# Python Virtual Environment on Windows

## References

1. [Download Python for Windows](https://www.python.org/downloads/windows/)
1. [How to Set Up a Python Virtual Environment on Windows 10](https://www.liquidweb.com/kb/how-to-setup-a-python-virtual-environment-on-windows-10/)
1. [PyPI Package: virtualenvwrapper-win](https://pypi.org/project/virtualenvwrapper-win/)

***
***

## Steps for Setting Up Python Virtual Environment on Windows 

### Step 1: Install Python

1. Download Python for Windows and install
1. To check installation:
    ```
    $ python --version
    ```

### Step 2: Install Pip

1. Pip should have been installed together with Python in Step 1
1. To check:
    ```
    $ pip --version
    ```

### Step 3: Install Virtualenv

1. Need to run as administrator
    ```
    $ pip install virtualenv
    ```

### Step 4: Set up a Virtual Environment

1. Create the virtual environment (This can be run as normal user)
1. In this example, standard-dev is the name of the virtual environment that we want to set up.
    ```
    $ mkdir standard-dev
    $ cd standard-dev
    $ virtualenv .
    $ cd ..
    ```
1. Activate the virtual environment
    ```
    $ .\standard-dev\Scripts\activate.bat
    ```
1. Deactivate the virtual environment
    ```
    (standard-dev) $ .\standard-dev\Scripts\deactivate.bat
    ```
    or simply
    ```
    (standard-dev) $ deactivate
    ```

### Step 5: Install virtualenvwrapper-win (Optional)

1. Installation of virtualenvwrapper-win is optional? (This is not done)
1. Need to run as administrator
1. Install globally, not in virtual environment
    ```
    $ pip install virtualenvwrapper-win
    ```

## Upgrade Pip

### Upgrade pip in main installation

1. This need to be run as administrator
    ```
    $ python -m pip install --upgrade pip
    ```

### Upgrade pip in virtual environment

1. This need to run after the virtual environment is activated
    ```
    (standard-dev) $ python -m pip install --upgrade pip
    ```

***
***

## Installing and Upgrading Packages for Virtual Environment

### Packages for standard development environment

1. Install everything:
    ```
    (standard-dev) $ pip install -r python-standard-dev-requirements.txt
    ```

1. Upgrade everything:
    ```
    (standard-dev) $ pip install -r python-standard-dev-requirements.txt --upgrade
    ```

### Packages for web development environment

1. Install everything
    ```
    (web-dev) $ pip install -r python-web-dev-requirements.txt
    ```

### Install Semgrep on Python in a virtual environment

    (See file tool-semgrep-installation.txt) (TODO)

***
*Updated on 1 August 2025*
