# Open Code Installation

## On Docker on Windows

Create Configuration Folder
```cmd
mkdir -p %USERPROFILE%\.config\opencode
```

Run Docker Image with Persistence
```cmd
docker run -it --rm --name opencode -v %USERPROFILE%\.config\opencode:/root/.config/opencode -v %CD%:/workspace -w /workspace ghcr.io/anomalyco/opencode
```

Pull Docker Model
```cmd
docker model pull qwen3-coder
```

Docker Model Setup Verification
```cmd
curl http://localhost:12434/v1/models
```

Reference: [OpenCode with Docker Model Runner for Private AI Coding](https://www.docker.com/blog/opencode-docker-model-runner-private-ai-coding/)

Sample %USERPROFILE%\.config\opencode\opencode.json
```
{
    "$schema": "https://opencode.ai/config.json",
    "provider": {
        "dmr": {
            "npm": "@ai-sdk/openai-compatible",
            "name": "Docker Model Runner",
            "options": {
                "baseURL": "http://localhost:12434/engines/llama.cpp/v1"
            },
            "models": {
                "qwen3-coder": {
                    "name": "qwen3-coder"
                },
                "gpt-oss": {
                    "name": "gpt-oss"
                }
            }
        }
    }
}
```

***
*Updated on 14 May 2026*
