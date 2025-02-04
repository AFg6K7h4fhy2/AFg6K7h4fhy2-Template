# Historical Repository Template Edits

_This document details historical iterations (especially `pre-commit` hooks) on the author's template repository (AFg6K7h4fhy2-Template)._

For Python `pre-commit` hooks:

```yaml
-   repo: https://github.com/psf/black-pre-commit-mirror
    rev: 25.1.0
    hooks:
    -   id: black
        args: ["--line-length", "79"]
        language_version: python3
-   repo: https://github.com/PyCQA/isort
    rev: 6.0.0
    hooks:
    -   id: isort
        args: [
          "--profile", "black",
          "--line-length", "79"]
        stages:
          - pre-commit
-   repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.7.2
    hooks:
      - id: ruff
        args: ["--ignore=E741", "--ignore=E731", "--fix"]
```
