# Build a Docker Image for OpenCode

## Build

```
docker build -t opencode-ubuntu .
```

## Run

```
docker run --rm -it --name opencode-ubuntu -v %USERPROFILE%\.config\opencode:/home/ubuntu/.config/opencode -v %CD%:/home/ubuntu/workspace -v %USERPROFILE%\.ssh\id_ed25519_github:/home/ubuntu/.ssh/id_ed25519 -v %USERPROFILE%\.ssh\id_ed25519_github.pub:/home/ubuntu/.ssh/id_ed25519.pub -w /home/ubuntu/workspace opencode-ubuntu bash
```

***
*Updated on 9 June 2026*
