FROM rust:1.87

RUN apt-get update && apt-get install -y \
    git \
    curl \
    pkg-config \
    build-essential \
    && rm -rf /var/lib/apt/lists/*