# Python style & testing guide

[&#8629; Contributing guidelines][contributing-guidelines]

- Please use a recent version of [Python 3][python] (3.6+)
- Please try to conform to the used code and commenting style within a project
  to maintain consistency
- Use [type hints][py-typing] for all function/method signatures (exception:
  tests)
- To improve consistency and allow the automatic generation of API docs, please
  stick to Python's [general docstring conventions][py-pep257] and follow
  [Google's docstring style][py-doc-style].
- Use the following linters with default settings:
  - [`flake8`][py-flake8]
  - [`mypy`][py-mypy] OR [`pyright`][py-pyright] to help with type hints
  - optional: [`black`][py-black]
- Use the following testing environments:
  - [`pytest`][py-pytest]

[contributing-guidelines]: contributing_guidelines.md
[py-black]: <https://github.com/psf/black>
[py-doc-style]: <https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html>
[py-flake8]: <https://gitlab.com/pycqa/flake8>
[py-mypy]: <http://mypy-lang.org/>
[py-pep257]: <https://www.python.org/dev/peps/pep-0257/>
[py-pyright]: <https://github.com/microsoft/pyright>
[py-pytest]: <https://docs.pytest.org/en/latest/>
[py-typing]: <https://docs.python.org/3/library/typing.html>
[python]: <https://www.python.org/>
