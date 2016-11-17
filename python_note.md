# Python Note
## List
* [Pyenv](#Pyenv)
* [Pip and easy_install](#pip-easy_install)

## To Do
* List and install needed python package
    - pip

<a name="Pyenv"></a>
## Pyenv
### Simple Python version management: [pyenv]
You can build your python develop environment without change or modify your host computer system python envioriment.

#### Install
```sh
$ curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash
```

#### Uninstall 
pyenv is installed within $PYENV_ROOT (default: ~/.pyenv). To uninstall, just remove it:
```sh
$ rm -fr ~/.pyenv
```
and remove these three lines from .bashrc:
```
export PATH="~/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

#### Install python using pyenv

List all versions of python
```sh
$ pyenv install --list
...
2.7.10
2.7.11
2.7.12
3.0.1
3.1
3.1.1
...
```

Install one of python versions
```sh
$ pyenv install 2.7.12
```
[Note] For this installation, it could also install pip for this python version. If not, you could install pip using easy_install.

```sh
$ easy_install pip
```

See python versions
```sh
$ pyenv versions
*  system
   2.7.12
```

Change python versions
```sh
$ pyenv global 2.7.12
   system
*  2.7.12
```

<a name="pip-easy_install"></a>
## Pip and easy_install

### Pip

#### Install and uninstall package
```sh
$ pip install [package_name]
$ pip uninstall [package_name]
```

#### Find out your python site-package path
For figure out the site-package localation in difference virtual environment.
You can use this command:
```sh
$ python -c "import site; print("\n".join(site.getsitepackages()))"

# For pyenv python 2.7.12 version
/Users/whlin/.pyenv/versions/2.7.12/Python.framework/Versions/2.7/lib/python2.7/site-packages
/Users/whlin/.pyenv/versions/2.7.12/Python.framework/Versions/2.7/lib/site-python
/Library/Python/2.7/site-packages

# For system python (original)
/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site-packages
/System/Library/Frameworks/Python.framework/Versions/2.7/lib/site-python
/Library/Python/2.7/site-packages
```

Every time you install new package in your python environment.
Use pip show package to see more detial:

```sh
$ pip show pyflakes
Name: pyflakes
Version: 1.3.0
Summary: passive checker of Python programs
Home-page: https://github.com/pyflakes/pyflakes
Author: A lot of people
Author-email: code-quality@python.org
License: MIT
Location: /Users/whlin/.pyenv/versions/2.7.12/Python.framework/Versions/2.7/lib/python2.7/site-packages
Requires:
```


How to list all installed packages and their versions in Python?
```sh
$ pip freeze
```

### Easy_install

#### Install package
```sh
$ easy_install [package_name]
```
It will install package to Install Package path. (ex: /Library/Python/2.7/site-packages)
It may install bin or script in /usr/local/bin

#### Uninstall package
Step:
* easy_install -m [package_name]
* Use pip uninstall tje package: pip uninstall [package_name]
* Remove bin or script of this package. Use which command to find it.

For example: (pyflakes)
```sh
# install
$ easy_install pyflakes     # Maybe sudo install

# uninstall
$ easy_install -m pyflakes
$ pip uninstall pyflakes
$ which pyflakes            # Find the bin or script
$ rm -rf $(which pyflakes)
```

You need to figure out what is going on when using pyenv and pip install package to build your develop environment.
When you use pip or easy_install to install package, where is the package? 
* The pyenv project architecture.
* pip install package flow

### Learn how to pip install python package for locally and globally

## Reference
* pyenv:
    - [yyuu/pyenv](https://github.com/yyuu/pyenv)
    - [yyuu/pyenv-installer](https://github.com/yyuu/pyenv-installer)
* pip and easy_install:
    - [link1](http://coopermaa2nd.blogspot.tw/2012/12/easyinstall-pip.html)
* [How to change default install location for pip](http://stackoverflow.com/questions/24174821/how-to-change-default-install-location-for-pip)
* [Install a Python package into a different directory using pip](http://stackoverflow.com/questions/2915471/install-a-python-package-into-a-different-directory-using-pip)
* [pyenv Command Reference](http://v2in.com/pyenv-installation-and-usage.html)
* [Simple Python Version Management: pyenv][pyenv]
* Introduct Python Package manager pip and easy_install: 
    * [link1](http://www.openfoundry.org/tw/tech-column/8536-introduction-of-python-extension-management-tools) 
    * [link2](http://coopermaa2nd.blogspot.tw/2012/12/easyinstall-pip.html)
* [pip document](https://pip.pypa.io/en/stable/)

[pyenv]: <https://github.com/yyuu/pyenv-installer>
