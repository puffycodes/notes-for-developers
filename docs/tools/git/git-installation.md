# Git Installation

## On MacOS

Install Xcode Command Line Tools:

1. Run any ```git``` command in the terminal. If git is not installed, a dialog box will appear prompting you to install the tools.
    ```bash
    git --version
    ```

Alternative (no done this way):

1. Install Homebrew.
1. Install git on Homebrew.
    ```bash
    brew install git
    ```

Configuration

1. See [Initial Configuration](#initial-configuration-recommended)

## On Linux

TODO

Configuration

1. See [Initial Configuration](#initial-configuration-recommended)

## On Windows

TODO

Configuration

1. See [Initial Configuration](#initial-configuration-recommended)

***
***

## Initial Configuration (Recommended)

After installation, set your name and email:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Verify the setting:
```bash
git config --global user.name
git config --global user.email
```

***
*Updated on 26 March 2026*
