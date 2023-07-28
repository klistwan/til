# Replacing future.utils.with_metaclass

`with_metaclass()` is a utility function to make it easier to develop code for both Python 2 and 3:

```python
from future.utils import with_metaclass

class UIDRelatedField(with_metaclass(ABCMeta, RelatedField)):
    pass
```

To remove usage of `future`, you can refactor it:

```python
class UIDRelatedField(RelatedFields, metaclass=ABCMeta):
    pass
```

Here is the code for `with_metaclass`:

```python
def with_metaclass(meta, *bases):
    """Create a base class with a metaclass."""
    # This requires a bit of explanation: the basic idea is to make a dummy
    # metaclass for one level of class instantiation that replaces itself with
    # the actual metaclass.
    class metaclass(type):

        def __new__(cls, name, this_bases, d):
            return meta(name, bases, d)

        @classmethod
        def __prepare__(cls, name, this_bases):
            return meta.__prepare__(name, bases)
    return type.__new__(metaclass, 'temporary_class', (), {})
```

References:
- [https://stackoverflow.com/a/18513858](https://stackoverflow.com/a/18513858)
