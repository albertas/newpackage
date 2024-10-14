# modernpackage
This package is configured using bleeding edge toolset and serves as an
example/starting point for another new packages.

## Development
Commonly used commands for package development:
- `make check` - run unit tests and linters.
- `make fix` - format code and fix detected fixable issues.
- `make publish` - publishes current package version to pypi.org.
- `make compile` - bump and freeze dependency versions in requirements*.txt files
- `make sync` - upgrade installed dependencies in Virtual Environment (executed after `make compile`)

## Toolset
This package uses these cutting edge tools:
- ruff - for linting and code formatting
- mypy - for type checking
- pip-audit - for known vulnerability detection in dependencies
- deadcode - for unused code detection
- pytest - for collecting and running unit tests
- coverage - for code coverage by unit tests
- hatch - for publishing package to pypi.org
- uv - for Python virtual environment and dependency management
- pyproject.toml - configuration file for all tools
- Makefile - aliases for commonly used command line commands

## Feature requests:
- Improve versioning by having single place to define a version like /__init__.py - pyproject should use version from there and it should be possible to import module and print its __version__.
- Add Makefile command to bootstrap the package (to override  name with a placeholder provided to the make file).
- codspeed.io could be considered for Continuous integration pipeline
