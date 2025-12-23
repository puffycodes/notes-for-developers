# SSH Key for GitHub

Reference: [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## Generate SSH Key

1. Generate a SSH key using ssh-keygen.

    ```
    > ssh-keygen -t ed25519 -C "your_email@example.com"
    ```

## Add SSH Key to the ssh-agent (Windows OS) (Optional?)

1.  In a new *admin elevated* PowerShell window, run the following commands.

    ```
    # start the ssh-agent in the background
    > Get-Service -Name ssh-agent | Set-Service -StartupType Manual
    > Start-Service ssh-agent
    ```

2. In a terminal window without elevated permission, add the SSH private key to the ssh-agent.

    ```
    > ssh-add c:\Users\YOU\.ssh\id_ed25519
    ```

## Add SSH public key to GitHub account

1.  Log in to GitHub and add the SSH public key.

    -   Users -> Settings -> SSH and GPG keys [(Link)](https://github.com/settings/keys)

## Non Standard SSH File Name

1.  If SSH file name is not a standard one (e.g. id_ed25519_github instead of id_ed25519), add the following lines to ~/.ssh/config.

    ```
    Host github.com
        HostName github.com
        IdentityFile ~/.ssh/id_ed25519_github
    ```

## Add or Change Passphase

1.  Change the passphase of a SSH key file.

    ```
    > ssh-keygen -p -f c:\Users\YOU\.ssh\id_ed25519
    ```

***

*Updated on 23 December 2025*
