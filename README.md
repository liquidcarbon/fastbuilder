# [`01 <- `](https://github.com/liquidcarbon/fastbuilder/tree/01)**`02`**[` -> 03`](https://github.com/liquidcarbon/fastbuilder/tree/03)

# Step 2.  Poetry

## 2.1. Create poetry environment

[Poetry](https://python-poetry.org/docs/) is a tool for dependency management and packaging in Python.  We will use it to install necessary packages.

```bash
git checkout 01
git checkout -b 02
poetry init
```

Output:
```
a@SNAVVV:~/code/fastbuilder$ poetry init

This command will guide you through creating your pyproject.toml config.

Package name [fastbuilder]:  
Version [0.1.0]:  
Description []:  Step-by-step tutorial for building a FastAPI data app
Author [liquidcarbon <akscrps@gmail.com>, n to skip]:  
License []:  
Compatible Python versions [^3.11]:  

Would you like to define your main dependencies interactively? (yes/no) [yes] no
Would you like to define your development dependencies interactively? (yes/no) [yes] no
Generated file

[tool.poetry]
name = "fastbuilder"
version = "0.1.0"
description = "Step-by-step tutorial for building a FastAPI data app"
authors = ["liquidcarbon <akscrps@gmail.com>"]
readme = "README.md"

[tool.poetry.dependencies]
python = "^3.11"


[build-system]
requires = ["poetry-core"]
build-backend = "poetry.core.masonry.api"


Do you confirm generation? (yes/no) [yes] yes
```

## 2.2. Install the virtual environment

```bash
poetry install
```

Output:
```
Creating virtualenv fastbuilder-GAaJdjFf-py3.11 in /home/a/.cache/pypoetry/virtualenvs
Updating dependencies
Resolving dependencies... (0.1s)
```

## 2.3. Bump the minor version

```bash
poetry version minor
```

Output:
```
Bumping version from 0.1.0 to 0.2.0
```