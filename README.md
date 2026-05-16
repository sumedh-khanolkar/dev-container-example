Test Rust project in dev container

### What is a dev container?

A dev container is a development environment inside a container. The idea is that your base machine is protected from any untoward changes introduced by the development process like certain types of supply chain attacks. The authoritative source is [containers.dev](https://containers.dev/).

### Pre-Requisites

- Install Docker engine (WSL users see below)
- Install VS Code
- Install Dev Containers extension

### Notice for WSL Users

If you are using WSL, then it is recommended that you install Docker engine in WSL. You will also need the WSL extension.

### Usage

- Clone the repo
- Open repo in VS Code
- In the Command Palette, run "Dev Containers: Open Folder in Container"

This will build the container according to the specs defined in `.devcontainer/devcontainer.json`, run the container, and open VS Code inside the container to the repo folder.

- In VS Code, you should see "Dev Container: Rust" or "Dev Container: Rust @ rootless" in the bottom left
- Go to the "Run and Debug" tab
- Click the "Start Debugging" button
- Observe that a new terminal opens and "Hello, world!" is printed to STDOUT

Alternatively, you can open this repo in a GitHub Codespace and start at the "Run and Debug" step.

### Repo structure

```
- .devcontainer/
    - devcontainer.json: Dev container specification
    - Dockerfile: Docker image recipe
- .vscode/
    - launch.json: Run configuration
- src/
    - main.rs: Source code
- .dockerignore: Docker ignore file
- .gitignore: Git ignore file
- Cargo.lock: Cargo lock file
- Cargo.toml: Cargo crate definition
- Dockerfile
- LICENSE: License file
- README.md: This file
```
