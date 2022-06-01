# Python


## pip (https://pypi.org/project/pip/)


pip is the package installer for Python. You can use pip to install packages from the Python Package Index and other indexes.
Ubuntu: `sudo apt install python3-pip`

## Python virtual environments (https://docs.python.org/3/library/venv.html)


`python3 -m venv tutorial-env`

Ubuntu: `apt install python3.9-venv`


`source ./bin/activate`


## Black autoformatter (https://black.readthedocs.io/en/stable/getting_started.html)


`pip install black`

## Autopep8 (https://pypi.org/project/autopep8/)

autopep8 automatically formats Python code to conform to the PEP 8 style guide. It uses the pycodestyle utility to determine what parts of the code needs to be formatted. autopep8 is capable of fixing most of the formatting issues that can be reported by pycodestyle.


## Python Diagnostic

https://docs.python.org/3/library/debug.html

## Scalene: a high-performance CPU, GPU and memory profiler for Python (https://github.com/plasma-umass/scalene)

Scalene is a high-performance CPU, GPU and memory profiler for Python that does a number of things that other Python profilers do not and cannot do. It runs orders of magnitude faster than other profilers while delivering far more detailed information.


## Where do I put my python files in the venv folder? (https://stackoverflow.com/questions/51499950/where-do-i-put-my-python-files-in-the-venv-folder)

*I guess you misunderstood the term "Virtual Environment". It provides an isolated environment wherein you can download a different version of python packages and run it for your project. Hence, do not put anything inside your virtual environment. Keep it clean.*

The virtual environment manages files which aren't yours. It doesn't care how you manage your own files. Put them wherever makes sense to you, just not anywhere inside the venv directory tree. Common solutions include directly in `myproject`, or in `myproject/src`.

## Beautiful soup and Selenium (https://www.crummy.com/software/BeautifulSoup/bs4/doc/):

*beautiful soup parses html. selenium actually opens and does shit inside your web browser clicking elements etc.*

Playwright is another good contender. https://playwright.dev/