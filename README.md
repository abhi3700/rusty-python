# rusty-python

Write Python rustically 🧑🏻‍💻🦀

## Installation

Install poetry using curl:

```sh
$ curl -sSL https://install.python-poetry.org | python3 -
```

Check if poetry is installed:

```sh
$ poetry --version
```

## Usage

### New project

Create a new project

```sh
$ poetry new rusty-python
```

This is the file directory structure:

```sh
├── README.md
├── pyproject.toml
├── rusty_python
│   ├── __init__.py
│   ├── greet.py
│   └── main.py
└── tests
    └── __init__.py
```

### Build

To check without building in order to save:

> Like `$ cargo check` command in Rust.

```sh
$ poetry check
All set!
```

To build:

```sh
$ poetry build
Building rusty-python (0.1.0)
  - Building sdist
  - Built rusty_python-0.1.0.tar.gz
  - Building wheel
  - Built rusty_python-0.1.0-py3-none-any.whl
```

### Lock

Generate a `poetry.lock` file:

```sh
$ poetry lock
```

Like `Cargo.lock`, `poetry.lock` is a file that records the exact versions of the dependencies that were used for a particular build.
And then one can use `$ poetry install` to install the exact versions of the dependencies.

### Run

Referring to the above directory structure, the following command will run the `main.py` file:

```sh
$ poetry run python3 -m rusty_python.main
```

And the following command will run the `greet.py` file:

```sh
$ poetry run python3 -m rusty_python.greet
```

### Test

```sh
$ poetry test
```

## Coding

Here are the things to note:

- `__init__.py` is a file that makes the directory a python package.
- `greet.py` a module that is a part of package `rusty_python`.
  > A module is a single file (or files) that are imported under one import and used. Package is a collection of modules in directories that give a package hierarchy.
- `main.py` a module that is a part of package `rusty_python`.

## References

- [Github](https://github.com/python-poetry/poetry) with 27k+ ⭐
- [Poetry Documentation](https://python-poetry.org/docs/)
