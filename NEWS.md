# Change log for cfg-diag library

## [Unreleased]

## [0.4.0] - 2022-10-22

### Breaking changes

- API break: restore the API of the `ConfigDiag*` class hierarchy: only
  a single `.diag()` method that accepts a fixed string. Add the new
  `Config*` class hierarchy with the `.diag(lambda)` and `.diag(string)`
  API

### Additions

- add Nix expressions for running the tests
- start a CONTRIBUTING.md document describing a possible workflow

### Fixes

- correctly refer to the `.diag_()` method for fixed strings in
  the documentation

## [0.3.1] - 2022-09-01

### Fixes

- relicense a unit test file to StorPool
- include the noxfile in the sdist tarball

### Other changes

- add the year 2022 to the copyright notices

## [0.3.0] - 2022-08-27

### Breaking changes

- API break: the `.diag()` method now accepts a callable function that
  will only be invoked if needed; it must return the string to be output

### Additions

- add the `.diag_()` method for strings that are not expensive to build
- list Python 3.11 as a supported version
- add a Nox definitions file

### Other changes

- various Tox configuration and testing clean-ups:
  - use Pylint 2.14; it no longer outputs the `no-self-use` lint
  - drop the flake8 + hacking environment, it is incompatible with recent
    versions of flake8
  - use `pytest.mark.parametrize()` instead of the ddt module
  - add both lower and upper version constraints to most of the package
    dependencies in the Tox test environments
  - move the mypy configuration to the pyproject.toml file
  - use types-setuptools and drop a `type: ignore` annotation

## [0.2.1] - 2022-02-28

### Fixes

- include the .editorconfig file in the sdist tarball

## [0.2.0] - 2022-02-28

### Additions

- add an EditorConfig definitions file
- add a flake8 + hacking Tox test environment

### Other changes

- drop Python 3.6 as a supported version, add Python 3.10 instead
- reformat the source code using black 22 and 100 characters per line
- drop the useless basepython definition from the Tox test environments
- add a pytest >= 6 dependency for the mypy environment and drop the type stubs
- reflow the tox.ini file with a four-character indent

## [0.1.1] - 2021-03-31

### Fixes

- fix a code comment
- add a manifest to include more files in the source distribution

### Other changes

- move some tool configuration options to setup.py and pyproject.toml
- add Python 3.9 as a supported version
- use unittest.mock instead of mock

## [0.1.0] - 2021-03-31

### Started

- first public release

[Unreleased]: https://github.com/storpool/python-cfg_diag/compare/release/0.4.0...main
[0.4.0]: https://github.com/storpool/python-cfg_diag/compare/release/0.3.1...release/0.4.0
[0.3.1]: https://github.com/storpool/python-cfg_diag/compare/release/0.3.0...release/0.3.1
[0.3.0]: https://github.com/storpool/python-cfg_diag/compare/release/0.2.1...release/0.3.0
[0.2.1]: https://github.com/storpool/python-cfg_diag/compare/release/0.2.0...release/0.2.1
[0.2.0]: https://github.com/storpool/python-cfg_diag/compare/release/0.1.1...release/0.2.0
[0.1.1]: https://github.com/storpool/python-cfg_diag/compare/release/0.1.0...release/0.1.1
[0.1.0]: https://github.com/storpool/python-cfg_diag/releases/tag/release%2F0.1.0
