# Build a Docker Image for OpenCode

## Build

```
docker build -t opencode-ubuntu .
```

## Run

```
docker run --rm -it --name opencode-ubuntu -v %USERPROFILE%\.config\opencode:/home/ubuntu/.config/opencode -v %CD%:/workspace -w /workspace opencode-ubuntu bash
```

***
*Updated on 8 June 2026*
