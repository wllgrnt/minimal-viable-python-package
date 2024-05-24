# cookiecutter-pypackage-minimal
Just pre-commit formatting, pytest, and mkdocs. (I am scared of tox)

Loosely based on https://waynerv.github.io/cookiecutter-pypackage/ with only the bare minimum necessary for Python dev work, because I do not want to have to think about Python packaging config ever again.

## Features
- poetry build system
- pre-commit hooks with flake8, black, and isort formatting
- mkdocs for anything in `docs/` (optional)
- pytest (optional)
- CLI with Click (optional) 
- TODO mkdocstrings (optional)
- TODO switch to ruff
- TODO add github tags

## Usage


### Installation
Make your repo on Github first, and clone it locally. Then:
- `pip install cookiecutter`
- `cookiecutter https://github.com/wllgrnt/cookiecutter-pypackage-minimal.git`

Note: this will install pre-commit as part of the installation process. It will also unpack itself into whatever directory you are currently in, **overwriting any existing files with the same names**.


Using poetry, the package is installed with `pip install` or `poetry install`. To include the dev dependencies, use:

`poetry install --with dev` or `pip install '.[dev]'`

(pyproject.toml doesn't use the newest pyproject.toml syntax to maintain pip installability)

 
### Testing
Run `pytest` from the repo root.

### Docs


### CLI
Whatever you decide to call your package, an executable with that name will be added to your PATH, which runs `cli.py:main()`. This can be configured using Click.
