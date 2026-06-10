# Build a Docker Image for OpenCode

## Build

```cmd
docker build -t opencode-ubuntu .
```

## Run

Run the docker container.
```cmd
docker run --rm -it --name opencode-ubuntu -v %USERPROFILE%\.config\opencode:/home/ubuntu/.config/opencode -v %CD%:/home/ubuntu/workspace -v %USERPROFILE%\.ssh\id_ed25519_github:/home/ubuntu/.ssh/id_ed25519 -v %USERPROFILE%\.ssh\id_ed25519_github.pub:/home/ubuntu/.ssh/id_ed25519.pub -w /home/ubuntu/workspace opencode-ubuntu bash
```

Start the Python virtual environment.
```bash
source ~/venv/bin/activate
```

Set those environment variables for graphify.
```bash
export GRAPHIFY_EXTRACT_URL="http://model-runner.docker.internal/engines/llama.cpp/v1"
export GRAPHIFY_MODEL_BACKEND="ollama" 
export GRAPHIFY_MODEL_NAME="qwen3-coder"
export OLLAMA_API_KEY="dummy"
```

Set up a directory for graphify in opencode.
```bash
cd <directory>
graphify install opencode
```

***
*Updated on 9 June 2026*
