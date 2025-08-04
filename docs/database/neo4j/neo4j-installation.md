# Installation of Neo4j

Reference: [Installation](https://neo4j.com/docs/operations-manual/current/installation)

## Local Installation On Windows (Community Version)

Reference: [Windows Installation](https://neo4j.com/docs/operations-manual/current/installation/windows)

1. Get [OpenJDK](https://openjdk.org) or [Oracle Java](https://www.oracle.com/java/technologies/downloads).
1. Download [Neo4j](https://neo4j.com/deployment-center).
1. Extract zip file to a permanent home on Windows, e.g. D:\neo4j\. This top level directory is referred to as NEO4J_HOME.
    1. To run Neo4j as a console application:
        ```
        <NEO4J_HOME>\bin\neo4j console
        ```
    1. To install Neo4j as a service:
        ```
        <NEO4J_HOME>\bin\neo4j windows-service install
        ```
        1. Start and stop service:
            ```
            <NEO4J_HOME>\bin\neo4j start
            <NEO4J_HOME>\bin\neo4j stop
            ```
1. Visit [http://localhost:7474](http://localhost:7474) in web browser.
1. Connect using username 'neo4j' with default password 'neo4j'.

## Install APOC Plugin on Local Installation

Reference: [APOC Installation](https://neo4j.com/labs/apoc/2025/installation)

1. Copy the apoc plugin (apoc-xxx.jar) from <NEO4J_HOME>\labs to <NEO4J_HOME>\plugins.
1. Add the following line to <NEO4J_HOME>\conf\neo4j.conf:
    ```
    dbms.security.procedures.unrestricted=apoc.*
    ```
1. Restart Neo4J
    ```
    neo4j restart
    ```

***
*Updated on 4 August 2025*
