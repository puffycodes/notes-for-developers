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

## Usage

1. [Preparing your code for CodeQL analysis](https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/preparing-your-code-for-codeql-analysis)

    ```
    codeql database create <database> --language=<language-identifier>
    ```

1. [Analyzing your code with CodeQL queries](https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/analyzing-your-code-with-codeql-queries)

    ```
    codeql database analyze <database> --format=<format> \
        --sarif-category=<language-specifier> --output=<output> \
        <packs,queries>
    ```

    E.g.
    ```
    codeql database analyze <database> --format=sarif-latest \
        --output=output.json --download codeql/python-queries:Functions
    ```

## Tutorial (TODO)

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
