# Activating a Python virtualenv in a Makefile

If you want to activate a virtualenv using `make`, you cannot do:

```make
install-deps:
    source .venv/bin/activate
    pip3 install -r requirements.txt
```

This doesn't work as intended because:

1. Recipes are executed in shell which may not understand `source`.
2. Each line of a recipe does `fork()`` its own shell so sourcing the virtual environment will not affect the subsequent lines.

Instead, your Makefile needs to be written as such:

```make
install-deps:
    . .venv/bin/activate ; \
    pip3 install -r requirements.txt
```

Source: [https://stackoverflow.com/a/60626643](https://stackoverflow.com/a/60626643)
