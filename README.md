## Seqera Studio VSCode

This repository contains the definition of Seqera Studio VSCode. The `main` branch contains the
latest supported version of VSCode with connect-client. To use an older version of any component,
check the existing tags using the pattern: `vscode/<version>/connect/<version>`.

## Components

- **[OpenVSCode Server](https://github.com/gitpod-io/openvscode-server) v1.101.2** — browser-based VS Code
- **[Nextflow](https://www.nextflow.io/)** — pre-installed and pre-warmed
- **Nextflow VS Code extension** — pre-installed for Nextflow workflow development
- **Python 3.13** — via micromamba/conda-forge
- **connect-client** — Seqera connect client for studio integration

## Repository Structure

`.seqera/` contains:

- `studio-config.yaml` — references the pre-built image; studios using this branch will not require a build step
- `Dockerfile` — shows how the image was built; fork this repository and modify it to create a custom image
- `env.yaml` — conda environment specification (Python 3.13, pip)
- `init` — startup script that launches the VSCode server

## Customization

To create a customized version:

1. Fork this repository
2. Modify the `Dockerfile` and/or `env.yaml` to add your tools or dependencies
3. Build and push your custom image
4. Update `studio-config.yaml` to reference your custom image

## Pre-built Image

The pre-built image is available at:

```
public.cr.seqera.io/platform/data-studio-vscode:1.101.2-0.12.1
```
