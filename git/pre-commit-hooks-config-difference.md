# What's the difference between `.pre-commit-hooks.yaml` and `.pre-commit-config.yaml`?

To use existing hooks, configure them in `.pre-commit-config.yaml`.
To write your own hooks, define them in `.pre-commit-hooks.yaml`.

For example, take this `.pre-commit-config.yaml` file:

```yaml
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v3.2.0
    hooks:
    -   id: trailing-whitespace
    -   id: mixed-line-ending
-   repo: https://github.com/psf/black
    rev: 20.8b1
    hooks:
    -   id: black
```

`pre-commit` looks at the two repositories with the specified git tags for a file
called `.pre-commit-hooks.yaml`.

References:

- [pre-commit hooks you must know](https://towardsdatascience.com/pre-commit-hooks-you-must-know-ff247f5feb7e)
