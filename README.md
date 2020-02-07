# Rabid Armadillo (aka Django App Template) [![Build Status](https://<travis_domain>/<your_travis_handle>/<your_repo_name>.svg?branch=master)](https://<travis_domain>/<your_travis_handle>/<your_repo_name>)


This is a template repository for when you want to create a new django app. It gives you, out of the box:
- preconfigured coverage
- preconfigured testing for a range of python, django versions using tox
- preconfigured django test app
- preconfigured travis.yml for CI
- preconfigured flake8
- preconfigured docs in .rst format (to publish to your_project.readthedocs.io)


## Template Repository

This is a template repository on GitHub. You can use it as a template when creating a new django app.


## How to use

### Start a repo

Create your own repository on github, using this repo as a template. Call it what you like. 
In this example, let's say your github username is `armadillo-queen` and your new repository is called `django-rabid-armadillo`.

### Replace template items

Do find and replace throughout, working your way through this list of replacements

| Search  | Replace (Example) | Description |
|-------|-------|-------|
| <your_repo_name> | `django-rabid-armadillo` | The github repository name. Convention for django apps seems to be hyphenating rather than using snake case, but do what you want. I assume the package name is the same as the gh repo name.|
| <your_github_handle> | `armadillo-queen` | Your github handle |                              
| <travis_domain> | `travis-ci.com` | Almost always `travis-ci.com` for me, but I think travis also have travis-ci.org for public stuff so make sure you're on the right domain. | 
| <your_travis_handle> | `armadillo-queen` | Possibly the same as your github handle, depends how you log into travis |
| <copyright_owner> | Tom Clark | The copyright owner's name. Probably you, or your company |
| `rabid_armadillo` | `rabid_armadillo` | The module name of your app, which is importable in python (ie hyphens don't work. Stick to snake case!). Search and replace the whole of everything! |
| `RabidArmadillo` | | Replace with the capitalised camel case version of your app name |
| `Rabid Armadillo` | Rabid Armadillo | Human-readable, capitalised, app name |

### Update setup.py

Add the library requirements under install_requires

### Update `LICENSE` file and `docs/source/license.rst`

Change the contents to an appropriate license for your project. Don't delete the LICENSE file, because it's bundled on the manifest onto the pypi deployment.

License is currently MIT. Do what you like, I guess, but I humbly beg you to keep it this way. There's nothing more 
frustrating than finding a library that does what you need, and that you could contribute to, then not being able to
use it because it's GPL'd.


### Deploy to pypi, travis and RTD

Instructions forthcoming. Google it. In the meantime...

This medium article descripbes the travis / releases integration steps:
    https://medium.com/@mikkokotila/deploying-python-packages-to-pypi-with-travis-works-9a6597781556

The Hitchiker's guide to python provides an excellent, standard, method for creating python packages:
    http://docs.python-guide.org/en/latest/writing/structure/

To deploy on PYPI follow the instructions at the bottom of:
    https://packaging.python.org/tutorials/distributing-packages/#uploading-your-project-to-pypi

