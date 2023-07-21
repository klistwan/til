# Using the `hash` function

If you hash an object in two different session, you won't get the same results:

```python
$ python3
Python 3.11.3 (main, Apr  7 2023, 21:05:46) [Clang 14.0.0 (clang-1400.0.29.202)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> hash("Hello world")
-1997592119266458120
```

```python
$ python3
Python 3.11.3 (main, Apr  7 2023, 21:05:46) [Clang 14.0.0 (clang-1400.0.29.202)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> hash("Hello world")
-6723738395645272785
```

This is because Python's `hash()` function is randomly "salted" when Python starts up (this started in Python 3.3, to prevent some denial-of-service attacks) [source](https://github.com/ageron/handson-ml3/blob/main/02_end_to_end_machine_learning_project.ipynb).

Further reading:
- The [original vulnerability disclosure](https://ocert.org/advisories/ocert-2011-003.html)
- [Discussion](https://github.com/python/cpython/issues/58826) on the Python issue tracker
