# `python-starter`

This is my project structure for new Python projects. It uses the following tools to automate the development process:

* `poetry`: Reproducible dependency management and packaging
* `tox`: Test and workflow automation against different Python environments
* `pytest`: Unittests
* `black`: Code formatting
* `isort`: Code imports formatting
* `flake8`: Code linting
* `mypy`: Static type checking

## Usage

Install [`poetry`](https://python-poetry.org/) on your machine if not yet installed. Install the project dependencies
using:

```shell
poetry install
```

You can invoke all workflows using the `tox` CLI:

```shell
tox -e format # Format code
tox -e lint # Lint code
tox -e format,lint # Format first and then lint
tox -e python3.10 # Run pytest tests for Python 3.10 environment

# Run all workflows in logical order:
# format -> lint -> pytest against all Python environments
tox
```
