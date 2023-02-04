# Docker driver installation guide

## Requirements

- Docker Engine

## Install

Please refer to the `Virtual environment`_ documentation for installation best
practices. If not using a virtual environment, please consider passing the
widely recommended `'--user' flag` when invoking ``pip``.

- Virtual environment: https://virtualenv.pypa.io/en/latest/
- `--user` flag: https://packaging.python.org/tutorials/installing-packages/#installing-to-the-user-site

```bash
$ pip install 'molecule[docker]'
```