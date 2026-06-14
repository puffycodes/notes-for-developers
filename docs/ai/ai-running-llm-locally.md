# Running LLM Locally

## Contents

1. [Hardware](#hardware)
1. Software
    1. [Docker Model Runner](#docker-model-runner)
    1. [LMStudio](#lmstudio)
    1. [Find the Right Local Model](#find-the-right-local-models)

## Hardware

1. Nvidia DGX Spark

    1. [DGX Spark User Guide](https://docs.nvidia.com/dgx/dgx-spark/index.html)

1. GMKTEC EVO-X2 AI Mini PC 128GB with Ryzen AI MAX+ 395

    1. [GMKtec](https://gmktec.com)

## Software

### Docker Model Runner

1. [Docker Model Runner](https://docs.docker.com/ai/model-runner/)
1. [Smol Models](https://github.com/huggingface/smollm)

#### Usage Example

Test:
```
docker model version
docker model run ai/smollm2
```

Run OpenAI gpt-oss with a single command:
```
docker model run ai/gpt-oss:20B
```

Pull and run Mistral model:
```
docker model pull ai/mistral:7B-Q4_0
docker model run ai/mistral:7B-Q4_0
```

Text to Image Model:
```
docker model pull hf.co/StableDiffusionVN/Flux:Q4_K_S
```

### LMStudio

1. [LMStudio](https://lmstudio.ai/)

### Find the Right Local Models

1. Check which models run well on your machine - [llmfit](https://github.com/AlexsJones/llmfit)
    ```bash
    docker run ghcr.io/alexsjones/llmfit
    ```

***
*Updated on 14 June 2026*
