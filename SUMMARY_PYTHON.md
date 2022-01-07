# Python

<!-- ## Package installer PIP https://pypi.org/project/pip/
pip is the package installer for Python. You can use pip to install packages from the Python Package Index and other indexes.

`sudo apt install python3-pip -y` -->

<!-- ## Virtual Environments https://docs.python.org/3/tutorial/venv.html

Python applications will often use packages and modules that don’t come as part of the standard library. Applications will sometimes need a specific version of a library, because the application may require that a particular bug has been fixed or the application may be written using an obsolete version of the library’s interface.

`python3 -m venv tutorial-env` -->

## pipx (https://github.com/pypa/pipx)

pipx — Install and Run Python Applications in Isolated Environments

## Python packaging and dependency management with poetry. (https://python-poetry.org/)

Using pipx to install Poetry is also possible. pipx is used to install Python CLI applications globally while still isolating them in virtual environments. This allows for clean upgrades and uninstalls. pipx supports Python 3.6 and later. If using an earlier version of Python, consider pipsi.

## Black autoformatter (https://black.readthedocs.io/en/stable/getting_started.html)

`pipx install black`
