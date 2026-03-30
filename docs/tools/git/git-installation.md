# Git Installation

## On MacOS

[Reference](https://git-scm.com/install/mac)

Install Xcode Command Line Tools:

1. Run any ```git``` command in the terminal. If git is not installed, a dialog box will appear prompting you to install the tools.
    ```bash
    git --version
    ```

Alternative (not done this way):

1. Install Homebrew.
1. Install git on Homebrew.
    ```bash
    brew install git
    ```

## On Linux

[Reference](https://git-scm.com/install/linux)

Installation on Debian or Ubuntu:
```bash
apt-get install git
```

## On Windows

Installation

1. Download from [here](https://git-scm.com/install/windows) and install.

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
*Updated on 30 March 2026*
