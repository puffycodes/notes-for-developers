# file: Dockerfile
# - Create a docker image for running OpenClaw

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

# Set up ssh directory for the 'ubuntu' user
RUN mkdir -p /home/ubuntu/.ssh && \
    chmod 700 /home/ubuntu/.ssh

# Add GitHub to the known_hosts file to avoid SSH warnings
RUN ssh-keyscan github.com >> /home/ubuntu/.ssh/known_hosts && \
    chmod 644 /home/ubuntu/.ssh/known_hosts

# Create the directory structure for the configuration files and fix ownership
RUN mkdir -p /home/ubuntu/.openclaw \
    && chown -R ubuntu:ubuntu /home/ubuntu/.openclaw

# Create a workspace directory to mount the project
RUN mkdir -p /home/ubuntu/workspace \
    && chown -R ubuntu:ubuntu /home/ubuntu/workspace

# Create a virtual environment to run openclaw
RUN mkdir -p /home/ubuntu/venv \
    && chown -R ubuntu:ubuntu /home/ubuntu/venv \
    && (cd /home/ubuntu/venv && python3 -m virtualenv .)

# Install the necessary packages in the virtual environment
RUN (. /home/ubuntu/venv/bin/activate && pip install graphifyy)

# Instlal OpenClaw
# https://openclaw.ai/
RUN curl -fsSL https://openclaw.ai/install.sh | bash

# --- end of file --- #
