# Python style & testing guide

[&#8629; Contributing guidelines][contributing-guidelines]

- Please use a recent version of [Python 3][python] (3.6+)
- Please try to conform to the used code, docstring and commenting style within
  a project to maintain consistency
- Use [type hints][py-typing] for all function/method signatures (exception:
  tests)
- Use the following linters with default settings:
  - [`flake8`][py-flake8]
  - [`mypy`][py-mypy] OR [`pyright`][py-pyright] to help with type hints
  - optional: [`black`][py-black]
- Use the following testing environments:
  - [`pytest`][py-pytest]

[contributing-guidelines]: contributing_guidelines.md
[py-black]: <https://github.com/psf/black>
[py-flake8]: <https://gitlab.com/pycqa/flake8>
[py-mypy]: <http://mypy-lang.org/>
[py-pyright]: <https://github.com/microsoft/pyright>
[py-pytest]: <https://docs.pytest.org/en/latest/>
[py-typing]: <https://docs.python.org/3/library/typing.html>
[python]: <https://www.python.org/>
