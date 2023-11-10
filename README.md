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

## Build

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

## Run

Referring to the above directory structure, the following command will run the `main.py` file:

```sh
$ poetry run python3 -m rusty_python.main
```

And the following command will run the `greet.py` file:

```sh
$ poetry run python3 -m rusty_python.greet
```
