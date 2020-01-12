# Python Learning Resources

These notes were made while teaching programing for beginners in Python. The resources are not structured as a tutorial but by topic, and they might be a good starting point for you.


- [Python Learning Resources](#python-learning-resources)
  - [IDE](#ide)
    - [Visual Studio Code](#visual-studio-code)
      - [Installation](#installation)
  - [Python Installation](#python-installation)
  - [Python Tools](#python-tools)
    - [PIP](#pip)
    - [Autoformatter](#autoformatter)
    - [Testing](#testing)
    - [Jupyter Notebook](#jupyter-notebook)
  - [Python Language](#python-language)
  - [Programming](#programming)
  - [Python Libs](#python-libs)

## IDE

The IDE (Integrated Development Environment) is fancy name for a *Code Editor* plus tools that makes you productive. There are penty out there and this is my short list:

- [PyCharm](https://www.jetbrains.com/pycharm/)
- [Visual Studio Code](https://code.visualstudio.com)

### Visual Studio Code

*Visual Studio Code* aka *Code*.
Pro: 
- If you use *Code* already (e.g. it's popular for *JavaScript*) you don't need to re-learn where to find the IDE features

#### Installation

Install the IDE: [Visual Studio Code](https://code.visualstudio.com)

Install the Python xxtension from Micro Soft:
  - https://marketplace.visualstudio.com/items?itemName=ms-python.python
  - Configuration: Follow the *details* on the extention page.


## Python Installation


Be aware, that there are some Python versions that are not compatible: Python version 2 and version 3.

Check which **version** your OS is using:
```console
$ which python
/usr/bin/python
$ ls -al /usr/bin/python
lrwxr-xr-x  1 root  wheel  75  9 Nov 08:52 /usr/bin/python -> [...]/bin/python2.7
```
You want to use [version 3](https://wiki.python.org/moin/Python2orPython3). Your OS (at least MacOS is) might depend on the version configured so better don't mess with it. Use *always* the long path to the right version like so: `/usr/bin/python3`

Check if python3 is installed:
```console
$ /usr/bin/python3 --version
Python 3.7.3
```


## Python Tools

### PIP

Pip is the *Python Package Installer*. Don't ask me why it's not called ppi. Maybe it's too hard to pronounce ;-)

Example: Use *pip* to install *pylint*:
```bash
/usr/bin/python3 -m pip install -U pylint --user
```
- `/usr/bin/python3`
  - path to python comand
- `-m pip`
  - "use module" pip
- `install -U`
  - install or upgrade
- `pylint`
  - package name to install
- `--user`
  - install the package not system wide but in the user's area

You can use the `--help` option to learn about comand line parameters:
```bash
/usr/bin/python3 --help
/usr/bin/python3 -m pip install --help
```

Put your user's directory with all python modules in your path. First learn where your directory is:
```console
$ /usr/bin/python3 -m site --user-base
/Users/<your-user-name>/Library/Python/3.7
```
Your *bin* directory is in the path. So in this example: `/Users/<your-user-name>/Library/Python/3.7/bin`.
Add this path to your PATH environment settings:
```bash
export PATH=$PATH:/Users/<your-user-name>/Library/Python/3.7/bin
```

### Autoformatter
Why using auto formatters?

[Autoformatters for Python](https://www.kevinpeters.net/auto-formatters-for-python):
> - You do not need a style guide for low-level problems since the auto formatter deals with those problems
> - This directly reduces the number of discussions about unnecessary things and let the developers focus on writing actual code
> - It will also help with onboarding developers on the codebase because the style of the code is consistent
> - Fewer merge conflicts since the style will almost always be the same

Popular formatters are: 
- [black](https://github.com/psf/black)
- [autoprep](https://github.com/hhatto/autopep8#features)
- [yapf](https://github.com/google/yapf#knobs)

I find them all not very satisfying in some cases when it comes to compact code. I go with *black* since it's suggested by [Prettier for Python](https://github.com/prettier/plugin-python).

```bash
/usr/bin/python3 -m pip install -U black --user
```

### Testing

- [pytest](https://github.com/pytest-dev/pytest)

```bash
/usr/bin/python3 -m pip install -U pylint --user
/usr/bin/python3 -m pip install -U pytest --user
```

### Jupyter Notebook

```bash
/usr/bin/python3 -m pip install -U jupyter --user
```

## Python Language

## Programming

## Python Libs
