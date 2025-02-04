# Python Dependency & Version Management Guide

* **Poetry**: Dependency management + virtual environments 
* **pyenv**: Python version installation/switching


## Poetry Essentials

#### Installation & Setup
```bash
# Install Poetry
curl -sSL https://install.python-poetry.org | python3 -

# New project 
poetry new my-project

# Existing project
poetry init
```

#### Key Commands
```bash
poetry add pandas         # Add package
poetry add -D pytest     # Add dev dependency 
poetry install          # Install all deps
poetry remove pandas    # Remove package
poetry run python ...   # Execute in venv
poetry shell           # Activate venv
```

#### Project Configuration (`pyproject.toml`)
```toml
[tool.poetry]
name = "my-project"
version = "0.1.0"
description = ""
authors = ["You <you@example.com>"]

[tool.poetry.dependencies]
python = "^3.9"         # Min Python version
pandas = "^2.0.2"

[tool.poetry.group.dev.dependencies]
pytest = "^7.4.0"
```
> You shouldn't need to manually edit this file or `poetry.lock` which is auto-generated.

#### Virtual Environment Management
```bash
poetry env info     # Show venv details
poetry env list     # List project venvs
poetry env use 3.11 # Specify Python version
```

## pyenv Essentials

#### Python Version Management
```bash
# List available versions
pyenv install --list

# Install specific version
pyenv install 3.11.4

# Set global version
pyenv global 3.11.4

# Set project-specific version (creates .python-version)
cd my-project
pyenv local 3.11.4
```

### Combined Workflow

1. Install Python version with pyenv:
```bash
pyenv install 3.11.4
pyenv global 3.11.4
```

2. Create Poetry project with specific Python:
```bash
poetry init    # Will use pyenv's 3.11.4
```

3. Verify environment:
```bash
poetry run python --version    # Python 3.11.4
```

4. Install dependencies:
```bash
poetry add numpy    # Installed in isolated venv
```
