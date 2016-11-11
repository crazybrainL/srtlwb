# Python Note

## Pyenv

Simple Python version management: [pyenv]

You can build your python develop environment without change or modify your host computer system python envioriment.


## Pip and easy_install

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

### Learn how to pip install python package for locally and globally

### Reference
* pyenv:
    - [yyuu/pyenv](https://github.com/yyuu/pyenv)
    - [yyuu/pyenv-installer](https://github.com/yyuu/pyenv-installer)
* pip and easy_install:
    - [link1](http://coopermaa2nd.blogspot.tw/2012/12/easyinstall-pip.html)
* [How to change default install location for pip](http://stackoverflow.com/questions/24174821/how-to-change-default-install-location-for-pip)
* [Install a Python package into a different directory using pip](http://stackoverflow.com/questions/2915471/install-a-python-package-into-a-different-directory-using-pip)

[pyenv]: <https://github.com/yyuu/pyenv-installer>
