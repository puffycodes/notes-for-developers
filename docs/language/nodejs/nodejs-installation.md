# Node.js Installation

## Node.js

1. [Node.js](https://nodejs.org/en)

## Download

1. [Node.js Download](https://nodejs.org/en/download)

## Installation On MacOS

1. Download prebuilt Node.js from above link for MacOS on ARM64.
1. Run the .pkg file and follow the instruction

## Upgrade on MacOS

1. Same process as installation above.

## Example Installation

```
node-v18.12.1.pkg:

This package will install:
	•	Node.js v18.12.1 to /usr/local/bin/node
	•	npm v8.19.2 to /usr/local/bin/npm

This package has installed:
	•	Node.js v18.12.1 to /usr/local/bin/node
	•	npm v8.19.2 to /usr/local/bin/npm
Make sure that /usr/local/bin is in your $PATH.
```

***
***

# Pnpm Installation

Preferred Method: Using Corepack (included with node.js):
```bash
corepack enable
corepack prepare pnpm@latest --activate
```

Note: ```corepack enable``` needs to run in Administrator mode on Windows.

Alternative Method: Using npm (Global Install):
```bash
npm install -g pnpm
```

***
*Updated on 9 March 2026*
