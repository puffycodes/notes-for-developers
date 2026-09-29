# Claude Code Installation

## Reference

1. [Claude Code Installation](https://code.claude.com/docs/en/setup)
1. [Quickstart](https://code.claude.com/docs/en/quickstart)

## Installation for MacOS, Linux or WSL

Installation:
```
curl -fsSL https://claude.ai/install.sh | bash
```

Check:
```
claude doctor
```

Usage:
```
cd your-awesome-project
claude
```

Authentication Options:
1. With [Claude's Pro or Max Plan](https://claude.ai)
2. With [Claude Console](https://console.anthropic.com)

Update:

Use
```
claude update
```

Uninstall:

Use
```
claude uninstall
```
or
```
rm -f ~/.local/bin/claude
```

## Installation for Windows

```cmd
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

Add ```%USERPROFILE%\.local\bin```: System Properties -> Environment Variables -> Edit User PATH -> New -> Add the path

***
*Updated on 29 September 2026*
