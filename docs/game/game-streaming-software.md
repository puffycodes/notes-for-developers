# Game Streaming Software

## Content

1. [Steam](#steam)
1. [Sunshine and Moonlight](#sunshine-and-moonlight)

## Steam

### Reference

1. [Steam Installation](https://store.steampowered.com/about/)

## Sunshine and Moonlight

### Reference

1. [Sunshine](https://github.com/lizardbyte/sunshine) and [Moonlight](https://moonlight-stream.org/)
1. [Sunshine Latest Documentation](https://docs.lizardbyte.dev/projects/sunshine/latest/)
1. [Ultimate Guide to Configure Sunshine + Moonlight for Remote Play](https://www.reddit.com/r/MoonlightStreaming/comments/1nmqalh/ultimate_guide_to_configuring_moonlight_sunshine/)
1. [Virtual Display Driver](https://github.com/VirtualDrivers/Virtual-Display-Driver)

### Installation Guide

1. [Sunshine Installation](https://docs.lizardbyte.dev/projects/sunshine/latest/md_docs_2getting__started.html)
    - Windows Installation
        - **Install Sunshine**
            - Download the .msi file for AMD64/x64. Run to install.
        - **Install ViGEmBus Driver**
            - Download installer (.exe) from [ViGEmBus Driver](https://github.com/nefarius/ViGEmBus/releases). Run to install.
            - Restart Windows after installation of driver.
            - Note: Do not install from Sunshine configuration page.
        - **Install Virtual Display Driver** (See Note)
            - Download installer (VDD.Control.xx.xx.xx.zip) from [VDD Release](https://github.com/VirtualDrivers/Virtual-Display-Driver/releases)
                - Unzip to a folder and run ```VDD Control.exe```
                - Click on ```Install Driver```
                - Restart Windows
            - Note: Necessary if the host is running as headless.
        - **Configuration**
            - Access [https://localhost:47990/](https://localhost:47990/) to set password
            - Note: Run ```dxgi-info.exe``` to see information on graphic cards and displays.
        - **Connect Client**
            - On client, start Moonlight client, select server and obtain PIN
            - On server, go to PIN tab, enter PIN and assign a host name

1. [Moonlight Installation](https://moonlight-stream.org/)
    - MacOS Installation
        - **Installation** Download the .dmg file for MacOS (Universal). Double click to open and drag ```Moonlight.app``` to ```Application```.
        - **Upgrade** Remove the ```Moonlight.app``` from ```Application``` and follow the Installation steps.
        - **Notes***
            - To disconnect a Moonlight session on MacOS, use Ctrl-Option-Shift-Q instead of Ctrl-Alt-Shift-Q.

***
*Updated on 27 May 2026*
