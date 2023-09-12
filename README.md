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

## 2.4. Commit and push

Notice how simple `git push` does not work, because our branch does not exist in the remote repo.  Once the first commit to a new remote branch is made, the subsequent commits can be pushed with `git push`.

```
a@SNAVVV:~/code/fastbuilder$ git status
On branch 02
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        poetry.lock
        pyproject.toml

no changes added to commit (use "git add" and/or "git commit -a")
a@SNAVVV:~/code/fastbuilder$ git add .
a@SNAVVV:~/code/fastbuilder$ git commit -m "poetry, with version bump"
[02 7a33c2a] poetry, with version bump
 3 files changed, 94 insertions(+), 86 deletions(-)
 rewrite README.md (96%)
 create mode 100644 poetry.lock
 create mode 100644 pyproject.toml
a@SNAVVV:~/code/fastbuilder$ git push
fatal: The current branch 02 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin 02

a@SNAVVV:~/code/fastbuilder$ git push -u origin 02
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.57 KiB | 1.57 MiB/s, done.
Total 5 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for '02' on GitHub by visiting:
remote:      https://github.com/liquidcarbon/fastbuilder/pull/new/02
remote: 
To https://github.com/liquidcarbon/fastbuilder.git
 * [new branch]      02 -> 02
Branch '02' set up to track remote branch '02' from 'origin'.
```