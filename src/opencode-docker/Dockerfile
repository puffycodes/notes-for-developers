# file: Dockerfile

# Use the latest Ubuntu image as the base image
FROM ubuntu:latest

# Set common environment variables
ENV DEBIAN_FRONTEND=noninteractive

# Install necessary tools and dependencies
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    gnupg \
    openssh-client \
    sudo \
    unzip \
    vim \
    wget \
    git \
    python3 \
    python3-pip \
    python3-virtualenv

# Install GitHub CLI (gj)
RUN curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | gpg --dearmor -o /usr/share/keyrings/githubcli-archive-keyring.gpg \
    && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
    && apt-get update \
    && apt-get install -y gh

# Clean up APT lists
RUN rm -rf /var/lib/apt/lists/*

# Add the 'ubuntu' user to the sudo group and allow passwordless sudo
RUN usermod -aG sudo ubuntu \
    && echo "ubuntu ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/ubuntu \
    && chmod 440 /etc/sudoers.d/ubuntu

# Set the existing non-root user 'ubuntu' as the default user
USER ubuntu

# Set the working directory to the home directory of the 'ubuntu' user
WORKDIR /home/ubuntu

# Install Python packages for the 'ubuntu' user
#RUN pip3 install --user graphifyy

# Set up ssh directory for the 'ubuntu' user
RUN mkdir -p /home/ubuntu/.ssh && \
    chmod 700 /home/ubuntu/.ssh

# Add GitHub to the known_hosts file to avoid SSH warnings
RUN ssh-keyscan github.com >> /home/ubuntu/.ssh/known_hosts && \
    chmod 644 /home/ubuntu/.ssh/known_hosts

# Create the directory structure for the auth file and fix ownership
# This prevents Docker from creating it as 'root' when the volume is mounted.
# This is important to be able to mount the OpenCode auth on docker run
#    -v ~/.local/share/opencode/auth.json:/home/ubuntu/.local/share/opencode/auth.json
RUN mkdir -p /home/ubuntu/.local/share/opencode \
    && chown -R ubuntu:ubuntu /home/ubuntu/.local/share/opencode

RUN mkdir -p /home/ubuntu/.config/opencode \
    && chown -R ubuntu:ubuntu /home/ubuntu/.config/opencode

# Create a workspace directory to mount the project
RUN mkdir -p /home/ubuntu/workspace \
    && chown -R ubuntu:ubuntu /home/ubuntu/workspace

# Install uv
# - uv is installed at /home/ubuntu/.local/bin/uv.
# - This is not added to the PATH while the Dockerfile is being built,
# - so the use of uv need to be specified with its full path.
#RUN curl -fsSL https://astral.sh/uv/install.sh | bash

# Install graphiffy
#RUN /home/ubuntu/.local/bin/uv tool install graphifyy

# Create a virtual environment to run opencode
RUN mkdir -p /home/ubuntu/venv \
    && chown -R ubuntu:ubuntu /home/ubuntu/venv \
    && (cd /home/ubuntu/venv && python3 -m virtualenv .)

# Install the necessary packages in the virtual environment
RUN (. /home/ubuntu/venv/bin/activate && pip install openai graphifyy)

# Install OpenCode AI
# https://opencode.ai/docs/
RUN curl -fsSL https://opencode.ai/install | bash

# --- end of file --- #
