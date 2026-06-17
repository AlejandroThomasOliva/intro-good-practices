# intro-good-practices

This repository is designed as a learning space where we will practice and apply software development best practices, including the use of Git, GitHub, Issues, Pull Requests, documentation, and collaborative work.

## Table of Contents

- [Tool Set](#tool-set)
- [Setting up a Virtual Environment](#setting-up-a-virtual-environment)
- [Requirements](#Requirements)

## Tool Set

The following external tools are used to initialize and manage the project:

| Name | Version |
| --- | --- |
| Python | >= 3.13 |
| Poetry | >= 2.4.1 |
| pyenv | >= v2.7.2 |

## Setting up a Virtual Environment

This project uses a local Python virtual environment to keep dependencies isolated from the global system installation.

> [!NOTE]
> Please be sure that you have the tool set suggested already installed on your local.

## Requirements

- Python >= 3.13
- `pyenv`

### Create the virtual environment

First, make sure Python 3.13 is selected for this project:

```powershell
pyenv local 3.13
```

Validate that it is 3.13.x

```powershell
python -V
```

This creates a local folder called .venv, which is ignored by .gitignore

```powershell
python -m venv .venv
```

Activates the virtual environment on Windows.

```powershell
.venv\Scripts\Activate.ps1
```
Install Poetry:

```powershell
pip install poetry
```

Install dependencies, including `dev` dependencies:

```powershell
poetry install --with=dev
```

Install the `pre-commit` configuration
```powershell
pre-commit install --hook-type commit-msg --hook-type pre-push
```