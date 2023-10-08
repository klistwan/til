# How do you add `gdformat` and `gdlint` as a pre-commit hook?

1. Create a file named `.pre-commit-config.yaml`

1. Add the following:

```yaml
repos:
-   repo: https://github.com/Scony/godot-gdscript-toolkit.git
    rev: 4.1.0
    hooks:
    -   id: gdlint
    -   id: gdformat
```

1. Run `pre-commit install`

1. Run against all files

```zsh
pre-commit run --all-files
```

References:

- [Zach Bernal's water shader](https://github.com/Chrisknyfe/boujie_water_shader/blob/25f3c2da458e0a4f65bdb5903dc068b050930c06/.pre-commit-config.yaml#L4)
- [pre-commit docs](https://pre-commit.com/)
