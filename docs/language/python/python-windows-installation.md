# Python Installation

## For Windows

Using Python install manager

1. Download Python install manager from [here](https://www.python.org.downloads/)
1. Run the .msix file
1. Get help for ```pymanager```
    ```cmd
    pymanager help
    ```
1. Update Python runtime, e.g. 3.14
    ```cmd
    pymanager install 3.14 --update
    ```
1. List Python runtime
    ```cmd
    pymanager list
    ```

Alternative

1. Download standalone installer from [here](https://www.python.org.downloads/)

## Installation of Packages for Windows

- Microsoft C++ Build Tools
    - Some packages need MSVC to build. See [Visual Studio Build Tools for C++](https://visualstudio.microsoft.com/visual-cpp-build-tools/).
        - Install 'Visual Studio Build Tools 20xx' with 'Desktop Development for C++'
- Enable Windows Long Path
    - Some packages need Windows Long Path Enabled. See [How to Enable Windows Long Path](https://pip.pypa.io/warnings/enable-long-paths).
        - Run gpedit.msc in terminal with Administrator rights to set.

***
*Updated on 17 April 2026*
