Python Project Template
=======================
Copyright 2020, 2021 Erich Blume <blume.erich@gmail.com>
Provided under the MIT License. See LICENSE for more information.

This project is a basic template for python projects. It uses:

* poetry for virtual environment management, dependency management, and package building
* mypy for static type analysis
* flake8 for static linting
* isort for opinionated formatting of package imports
* black for opinionated formatting of the rest of python code
* pytest-xdist (and other pytest plugins) for test automation and enhancement.
* pre-commit to handle code correctness enforcement
* and more...

About The Template
------------------

This readme, and all of the code in this project, refers to this template
project as `your_project` as a placeholder. You can find the `your_project`
package in `root/src/your_project/`.

To use this template, simply check it out and begin the process of renaming the
`your_project` package. To do this, first rename `root/src/your_project` and
edit `pyproject.toml` to reflect your new python project. From there, any
remaining references to `your_project` should automatically result in errors
during static analysis or testing, and so you may fix them as you resolve those
errors.

Depending on how you cloned/retrieved this template, you may also wish to remove
your `origin` remote in git via `git remote remove origin`.

How to Install
--------------

These instructions refer to how you may instruct users of your project to
install your project. To understand how to use this template, please see `About
the Template`.

This template uses `poetry` to manage dependency management and other build
related processes. `poetry` includes the ability to publish packages to PyPI,
and also allows users to easily import and manage your project via github
repository links or harcoded filepaths, and even supports 'editable' mode
installations. See https://python-poetry.org/docs/cli/#add for more information
on how users may install your package using `poetry`.

While you should use `poetry` to develop this package, your users are not
FORCED to use poetry. They can also simply use `pip` or whichever other build
tool they wish to use, including sdist/wheels.

How to Test
-----------

This template uses `pyproject.toml` to track all root and development
dependencies, including the entire build chain. `poetry` is used to.
handle installing the project and all dependencies. `pytest` is used to run
test sessions.

1. Install `poetry` and initialize a new poetry environment.

   ```bash
   # Install poetry on a POSIX system (installation is 'upgrade-or-idempotent')
   # (a Windows installer exists as well, see python-poetry.org)
   $ curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python
   $ poetry install
   ```

   (NB: You can also just `pip install poetry`, but this has
   [known issues](https://python-poetry.org/docs/#alternative-installation-methods-not-recommended).)

2. Run the test suite

   ```bash
   $ poetry run pytest
   # Alternatively:
   $ poetry shell
   your_project-env $ pytest
   ```

How to Develop
--------------

Before doing any development on your project, please install `poetry` as per
option 1 of the "How to Test" section, above. **Then, please run the following**:

```bash
$ poetry run pre-commit install
```

This will install a number of pre-commit hooks in your local clone of this
repository, which will ensure that you can't commit code that will break
Funicular. (You can bypass this with `git commit --no-verify`, but please be
careful.)

How to Discuss
--------------

If you have design suggestions, questions, or bug reports - please file an
Issue on this github project. You can also email me at blume.erich@gmail.com,
but to be honest, I'm not the best at checking my email. Issues are more likely
to be seen.

How to Contribute
-----------------

Please see "How to Develop", and then submit a PR! It's fine to submit partial
PRs and/or pseudocode. I don't bite.
