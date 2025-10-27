# Amazon Q Developer

## References

1. [Amazon Q Documentation](https://docs.aws.amazon.com/amazonq/)
1. [Install Amazon Q Developer CLI](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html)
1. [Install Amazon Q Developer CLI on Windows](https://dev.to/aws/the-essential-guide-to-installing-amazon-q-developer-cli-on-windows-lmh)

***
***

## Install Amazon Q Developer CLI for Windows

### Install WSL

```
wsl --install
```

### Install Amazon Q Developer CLI

Start/Install Ubuntu on WSL
```
wsl -d Ubuntu
```

Change Working Directory (Install in /home/{youruser} directory)
```
cd
```

Install the necessary tools for WSL
```
sudo apt install unzip
```

Download Installer (Should be in /home/{youruser} directory)
```
curl --proto '=https' --tlsv1.2 -sSf "https://desktop-release.q.us-east-1.amazonaws.com/latest/q-x86_64-linux-musl.zip" -o "q.zip"
```

Unzip the Installer
```
unzip q.zip
```

Enable the Installer
```
cd q
chmod +x install.sh
```

Run the Installer
```
./install.sh
```

Answers when prompted
```
Do you want q to modify your shell config (you will have to manually do this otherwise)? · Yes
Select login method · Use for Free with Builder 
```

Re-launch WSL or use the following to update the shell configuration
```
bash
```

### Using Amazon Q Developer CLI

Login to Amazon Q Developer CLI (with AWS Builder ID)
```
q login
```

Run Amazon Q Developer CLI
```
q chat
```

Exit Amazon Q Developer CLI
```
/q
```

***
***

## Install Amazon Q Developer CLI for MacOS

1. [Download Amazon Q for command line for macOS.](https://desktop-release.q.us-east-1.amazonaws.com/latest/Amazon%20Q.dmg)
1. Double-click on the downloaded .dmg file and drag the app into your applications folder.
1. In your applications folder, double-click on Amazon Q. The GUI will open.
1. Enable the shell integrations.
1. Authenticate with Builder ID.
1. Follow the instructions to install the shell integrations.

To disable Amazon Q AI-powered inline completions:
```
q inline disable
```

To disable Amazon Q shell auto-completion:

1. Comment away the relevant line(s) in ~/.zshrc or ~/.bashrc or ~/.bash_profile.

***
***

***
*Updated on 3 October 2025*
