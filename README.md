# [`02 <- `](https://github.com/liquidcarbon/fastbuilder/tree/02)**`03`**[` -> 04`](https://github.com/liquidcarbon/fastbuilder/tree/04)

# Step 3.  Add a package and make an HTTP request

## 3.1. Add `requests`

```bash
poetry add requests
```

Output:
```
Using version ^2.31.0 for requests

Updating dependencies
Resolving dependencies... (0.2s)

Package operations: 5 installs, 0 updates, 0 removals

  • Installing certifi (2023.7.22)
  • Installing charset-normalizer (3.2.0)
  • Installing idna (3.4)
  • Installing urllib3 (2.0.4)
  • Installing requests (2.31.0)

Writing lock file
```

## 3.2. Check execution environment

To run commands from within Poetry's virtual environment, prefix familiar commands with `poetry run`.  First, let's check what is the python executable associated with our repo.  Notice how the output is different from plain `which python`:

```bash
which python; poetry run which python
```

Output:
```
/home/a/.pyenv/shims/python
/home/a/.cache/pypoetry/virtualenvs/fastbuilder-GAaJdjFf-py3.11/bin/python
```

Similarly, `pip install ...` will place a new package into the base python environment.  We will normally use `poetry add ...` to install packages and its dependencies.  Counterintuitively, to add a package to the current environment without the help of poetry, use `poetry run pip install ...`.

## 3.2. Use `requests` to make an API call

Let's find out where the [International Space Station](https://wheretheiss.at/w/developer) is at.

```bash
poetry run python -c 'import requests; response = requests.get("https://api.wheretheiss.at/v1/satellites/25544"); print(response.json())'
```

Output:
```
{'name': 'iss', 'id': 25544, 'latitude': -35.713143945496, 'longitude': 59.38801936154, 'altitude': 428.37857180456, 'velocity': 27559.613154356, 'visibility': 'daylight', 'footprint': 4549.8465802582, 'timestamp': 1694517856, 'daynum': 2460199.9751852, 'solar_lat': 4.1732364027409, 'solar_lon': 8.0299898605422, 'units': 'kilometers'}
```

Running `curl -s https://api.wheretheiss.at/v1/satellites/25544` should produce a similar result.


