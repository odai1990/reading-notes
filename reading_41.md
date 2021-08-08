# Read 41
## Pythonisms
[Dunder Methods](https://dbader.org/blog/python-dunder-methods)

Dunder methods are predefined methods that can be use in classes. 

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:

```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
```
To fix this, you can add a __len__ dunder method to your class:
```
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

[Iterators](https://dbader.org/blog/python-iterators)

[Generators](https://dbader.org/blog/python-generators)

Generators produce a sequence of values. Could be a sequence of integers, booleans, strings, any type of value. Generators are functions than can pause and resume later when they are called. 
It uses the keyword **yeild**