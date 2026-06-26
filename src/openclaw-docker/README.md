# Build a Docker Image for OpenClaw

## Build

```cmd
docker build -t openclaw-ubuntu .
```

## Run

On Linux/MacOS:

- Prepare the folders
    ```bash
    mkdir openclaw-workspace
    cd openclaw-workspace
    mkdir .openclaw workspace
    ```
- Run OpenClaw (TODO: Need to test this.)
    ```bash
    cd openclaw-workspace
    docker run --rm -it --name openclaw-ubuntu -v .openclaw:/home/ubuntu/.openclaw -v workspace:/home/ubuntu/workspace openclaw-ubuntu bash
    ```

***
*Updated on 26 June 2026*
