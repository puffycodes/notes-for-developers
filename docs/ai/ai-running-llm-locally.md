# Running LLM Locally

## Nvidia DGX Spark (Hardware)

Reference: [DGX Spark User Guide](https://docs.nvidia.com/dgx/dgx-spark/index.html)

## Docker Model Runner

Reference: [Docker Model Runner](https://docs.docker.com/ai/model-runner/)

Test:
```
docker model version
docker model run ai/smollm2
```

### Examples

Run OpenAI gpt-oss with a single command:

```
docker model run ai/gpt-oss:20B
```

Pull and run Mistral model:

```
docker model pull ai/mistral:7B-Q4_0
docker model run ai/mistral:7B-Q4_0
```

Text to Image:

```
docker model pull hf.co/StableDiffusionVN/Flux:Q4_K_S
```

## LMStudio

Reference: [LMStudio](https://lmstudio.ai/)

***
*Updated on 23 December 2025*
