# Metasploit Framework Installation

## Reference

1. [Metasploit Documentation](https://docs.metasploit.com/)
1. [Installing Metasploit Framework](https://docs.metasploit.com/docs/using-metasploit/getting-started/nightly-installers.html#installing-metasploit-on-linux--macos)

## Installation

On Linux/MacOS:
```
curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
  chmod 755 msfinstall && \
  ./msfinstall
```

Run:
```
msfconsole
```

***
*Updated on 5 May 2026*
