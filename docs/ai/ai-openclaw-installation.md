# OpenClaw

## References

1. [OpenClaw](https://openclaw.ai/)
1. [OpenClaw Local Installation](https://www.tencentcloud.com/techpedia/140023)
    - This guide refers to the use of Java, while the GitHub repository contains code for typescript.
1. [OpenClaw - Getting Started](https://docs.openclaw.ai/start/getting-started)

## Installation

### On Linux and MacOS (With Admin Rights)

```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

### Install Without Admin Rights

[Install from Source](https://docs.openclaw.ai/install#from-source)

Using pnpm:
```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw
pnpm install
pnpm ui:build
pnpm build
pnpm openclaw onboard --install-daemon
```

***
*Updated on 9 March 2026*
