# Starter Template - vscode-docker-xeus-cling

A Docker container pre-configured to run C++ Jupyter Notebooks in VS Code.

# Installation

Make sure to have the following installed:

- [Docker](https://www.docker.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [VS Code Remote - Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Installation by cloning this repository

Close this repository into your preferred location.

```sh
git clone https://github.com/ShuHighBridge/vscode-docker-xeus-cling.git
```

Open the cloned repository. Proceed when VS Code prompts to reopen in a Dev Container session. To open this repository straight into dev container mode, you may wish to install the VS Code CLI.

See [VS Code Docs - Opening a folder directly within a dev container](https://code.visualstudio.com/docs/remote/devcontainer-cli#_opening-a-folder-directly-within-a-dev-container)

Confirm installtion by running `examples/hello.ipynb`. Before running, make sure to select an appropriate C++ kernel on top-right of the VS Code UI. The C++ 11 or 14 kernel located inside `/opt/conda/envs/cling/bin/xcpp` seem to work correctly.

# About this Configuration

This container pulls its base image from the python-3-miniconda image available from the [vscode-dev-containers](https://github.com/microsoft/vscode-dev-containers) by Microsoft. This is a Debian container that comes with Python, Miniconda and other necessary tools pre-configured.

On top of the base image, this image installs [xeus-cling](https://github.com/jupyter-xeus/xeus-cling) and [Jupyter Lab](https://jupyter.org/) and configures the `cling` conda environment to be used without any additional configuration.