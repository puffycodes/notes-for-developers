# CodeQL

## References

1. [CodeQL](https://codeql.github.com)
1. [CodeQL Quickstart](https://marketplace.visualstudio.com/items?itemName=github.vscode-codeql)
1. [CodeQL Tutorial](https://codeql.github.com/docs/writing-codeql-queries/ql-tutorials)

## Installation

### Installing CodeQL CLI and VSCode Extension

1. For CLI: Download [latest release](https://github.com/github/codeql-cli-binaries/releases).
    - Install in path, e.g. C:\Program Files\codeql
    - Add the path to your system path
1. For VSCode: Install CodeQL extension from Visual Studio Marketplace.
    - Check using command CodeQL: Check for CLI Updates
    - Find the commands in Command Palette (Ctrl+Shift+P or Cmd+Shift+P) and by typing CodeQL.

### Cloning the CodeQL starter workspace

1. Clone the starter workspace
    ```
    git clone --recursive https://github.com/github/vscode-codeql-starter/
    ```
1. Update the starter workspace
    ```
    git pull
    git submodule update --recursive
    ```

### Importing a database from GitHub

<TODO>

***
*Updated on 6 August 2025*
