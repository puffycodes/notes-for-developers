# Open Code Installation

## Reference

1. [OpenCode](https://opencode.ai/)
1. [OpenCode Provider](https://opencode.ai/docs/providers)
1. [OpenCode with Docker Model Runner for Private AI Coding](https://www.docker.com/blog/opencode-docker-model-runner-private-ai-coding/)
1. [DMR REST API](https://docs.docker.com/ai/model-runner/api-reference/)
1. [How to run OpenCode AI in a Docker container](https://agileweboperations.com/2025/11/23/how-to-run-opencode-ai-in-a-docker-container/)

## On Docker on Windows

Create Configuration Folder
```cmd
mkdir -p %USERPROFILE%\.config\opencode
```

Run Docker Image with Persistence
- OpenCode Docker Image
    ```cmd
    docker run -it --rm --name opencode -v %USERPROFILE%\.config\opencode:/root/.config/opencode -v %CD%:/workspace -w /workspace ghcr.io/anomalyco/opencode
    ```
- OpenCode CLI
    ```cmd
    docker run -it --rm --name opencode-cli -v %USERPROFILE%\.config\opencode:/home/node/.config/opencode -v %CD%:/workspace -w /workspace nezhar/opencode-cli
    ```

Pull Docker Model
```cmd
docker model pull gpt-oss
docker model pull qwen3-coder
```

Docker Model Setup Verification
- From Host
    ```cmd
    curl http://localhost:12434/v1/models
    ```
- From Container
    ```cmd
    curl http://model-runner.docker.internal/v1/models
    ```

Sample %USERPROFILE%\.config\opencode\opencode.json for Docker Container
```
{
    "$schema": "https://opencode.ai/config.json",
    "provider": {
        "dmr": {
            "npm": "@ai-sdk/openai-compatible",
            "name": "Docker Model Runner",
            "options": {
                "baseURL": "http://model-runner.docker.internal/engines/llama.cpp/v1"
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

OpenCode Skills File Directory

1. Create the skill file directory
    ```cmd
    mkdir -p %USERPROFILE%\.config\opencode\skills
    ```
1. Copy the skill files to the skill file directory
    ```cmd
    mkdir -p %USERPROFILE%\.config\opencode\skills\<skill_name>
    copy <skill_name>\SKILL.md %USERPROFILE%\.config\opencode\skills\<skill_name>
    ```

***
*Updated on 1 June 2026*
