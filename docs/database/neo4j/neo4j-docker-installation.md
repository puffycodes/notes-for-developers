# Neo4J Graph Database

## Community Version

Reference: [Download](https://neo4j.com/deployment-center/?gdb-selfmanaged&community)

1. Download ...

## Docker Version

Reference: [Neo4J at Docker Hub](https://hub.docker.com/_/neo4j)

1. Pull the docker image:
    ```
    docker pull neo4j
    ```
1. Run with:
    ```
    docker run --rm \
        --publish=7474:7474 --publish=7687:7687 \
        --volume=$HOME/neo4j/data:/data \
        neo4j
    ```
    1. Specify the following to docker run to disable authentication:
        ```
        --env=NEO4J_AUTH=none
        ```
1. Connect to http://localhost:7474
1. Stop docker with Ctrl-C

***
*Updated on 13 July 2025*
