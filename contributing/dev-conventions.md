---
description: How to work with the existing cellfinder developers
---

# Development conventions

## Pull requests

In all cases, please submit code to the main repository via a pull request. Upon approval, please merge via "Squash and Merge" on GitHub to maintain a clean commit history.

Please submit pull requests as early as possible \(you can still push to the branch once submitted\) to allow discussion.

## Formatting

cellfinder uses [Black](https://github.com/python/black) and [Flake8](https://flake8.pycqa.org/en/latest/) to ensure a consistent code style. Please run `pre-commit install` prior to working on the code to ensure that these tests are run on each commit.

To check your code before committing, please run:

```python
black ./
flake8
```

## Testing

`cellfinder` uses [pytest](https://docs.pytest.org/en/latest/) for testing. Please try to ensure that all functions are tested in `tests/tests/test_unit` and all workflows/command-line tools are tested in `tests/tests/test_integration`.

Some tests may take a long time \(e.g. those requiring tensorflow if you don't have a GPU\). These tests should be marked with `@pytest.mark.slow`, e.g.:

```python
import pytest
@pytest.mark.slow
def test_something_slow():
    slow_result = run_slow_processes()
    assert slow_result == expected_slow_thing
```

During development, these "slow" tests can be skipped by running `pytest -m "not slow"`.

## Travis

All commits & pull requests will be build by [Travis](https://travis-ci.com). To ensure there are no issues, please check that it builds: `pip install .` and run all of the tests: `pytest` before committing changes.

## Dependencies

The code in the cellfinder repository should be primarily for cell detection. Other changes should be added to the relevant repository:

* **Regstration:** [brainreg](https://github.com/brainglobe/brainreg)
* **Image data IO:** [imio](https://github.com/adamltyson/imio)
* **General imaging processing \(and other\) tools:**  [imlib](https://github.com/adamltyson/imlib).

## File paths

All file paths should be defined in `cellfinder.tools.prep.Paths`. Any intermediate file paths, \(i.e. those which are not of interest to the typical end user\) should be prefixed with `tmp__`. These should then be cleaned up as soon as possible after generation.

