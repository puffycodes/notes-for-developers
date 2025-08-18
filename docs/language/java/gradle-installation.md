# Gradle Installation

## Reference

1. [Gradle Installation](https://gradle.org/install/)

## Installation Steps

### Prerequisites

Need [Java JDK](java-installation.md) version 8 or higher. To check:
```
java -version
```

### Install Manually for Windows

1. [Download the installer](https://gradle.org/releases/)
1. Unpack the distribution
    1. Create a new directory C:\Gradle (or C:\Program Files\Gradle).
    1. Unpack the folder gradle-x.x.x to the new directory.
1. Set up system path
    1. Add C:\Gradle\gradle-x.x.x\bin (or C:\Program Files\Gradle\gradle-x.x.x\bin) to System Variables -> Path
1. Verify installation
    ```
    gradle -v
    ```

***
*Updated on 18 August 2025*
