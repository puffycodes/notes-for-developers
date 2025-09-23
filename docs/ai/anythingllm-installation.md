# AnythingLLM

## References

1. [AnythingLLM](https://anythingllm.com/)

## Installation

1. [Install for Desktop](https://anythingllm.com/desktop)

1. [Install for Docker](https://docs.anythingllm.com/installation-docker/local-docker)

    1. Pull docker image:
        ```
        docker pull mintplexlabs/anythingllm:latest
        ```
    1. Start docker with the following script on Linux/Mac:
        ```
        export STORAGE_LOCATION=$HOME/anythingllm && \
        mkdir -p $STORAGE_LOCATION && \
        touch "$STORAGE_LOCATION/.env" && \
        docker run -d -p 3001:3001 \
        --cap-add SYS_ADMIN \
        -v ${STORAGE_LOCATION}:/app/server/storage \
        -v ${STORAGE_LOCATION}/.env:/app/server/.env \
        -e STORAGE_DIR="/app/server/storage" \
        mintplexlabs/anythingllm
        ```
    1. Visit ```http://localhost:3001``` on browser

***
*Updated on 23 September 2025*
