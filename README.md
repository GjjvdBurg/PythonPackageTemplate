# Python Package Skeleton

This repository contains a script ``create_package.py`` that generates a 
template directory for a new Python package. The generated package uses 
[poetry](https://poetry.eustace.io/) for packaging, 
[Travis](https://travis-ci.org/) for continuous integration, 
[Sphinx](https://www.sphinx-doc.org/en/master/index.html) with 
[autodoc](https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html) 
and [Read the Docs](https://readthedocs.org/) for documentation, and 
[Green](https://github.com/CleanCut/green) for unit testing. It also comes 
with a handy Makefile that ties everything together.

This script was created because I don't want to reinvent the wheel everytime I 
create a new Python package. Hopefully it's useful for others too. If you find 
a problem, please open an issue or submit a pull request.

The script takes a package name as command line argument:

```bash
python create_package.py newpkg
```

and creates the following package structure:

```
├── CHANGELOG.md
├── docs
│   ├── _build
│   ├── changelog.rst
│   ├── conf.py
│   ├── index.rst
│   ├── make.bat
│   ├── Makefile
│   ├── readme.rst
│   ├── source
│   ├── _static
│   └── _templates
├── Makefile
├── make_release.py
├── MANIFEST.in
├── newpkg
│   ├── __init__.py
│   └── __version__.py
├── poetry.lock
├── pyproject.toml
├── README.md
└── setup.py
```

**Note:** The generated package doesn't yet fully use Poetry for packaging and 
publishing the Python package and instead relies on a separate ``setup.py`` 
and a generated ``requirements.txt``. Doing all this using Poetry is planned 
for the future.
