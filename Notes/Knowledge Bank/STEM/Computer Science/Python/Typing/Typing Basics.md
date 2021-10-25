### Typing Basics

Typing is used on function arguments, like this
```python
def greeting(name: str) -> str:
    return 'Hello ' + name
```

Here is a list of the non-obvious Stuff
 ```python
 from typing import Iterable, Union, Optional, Callable, List, Any
 def f(num1: int, my_float: float = 3.5) -> float:
       return num1 + my_float
  # This is how you anotate callable functions
  x: Callable[[int, float], float] = f
  
 ```
 
 To reveal the type, use 
 ```python
 reveal_type(1) # Will print an error message with the type. 
 ```
 
 Standard duck types are for objects that behave in certain ways.
 ```python
 from typing import Mapping, MutableMapping, Sequence, Iterable, List, Set

# Use Iterable for generic iterables (anything usable in "for"),
# and Sequence where a sequence (supporting "len" and "__getitem__") is
# required
def f(ints: Iterable[int]) -> List[str]:
    return [str(x) for x in ints]

f(range(1, 3))

# Mapping describes a dict-like object (with "__getitem__") that we won't
# mutate, and MutableMapping one (with "__setitem__") that we might
def f(my_mapping: Mapping[int, str]) -> List[int]:
    my_mapping[5] = 'maybe'  # if we try this, mypy will throw an error...
    return list(my_mapping.keys())

f({3: 'yes', 4: 'no'})

def f(my_mapping: MutableMapping[int, str]) -> Set[str]:
    my_mapping[5] = 'maybe'  # ...but mypy is OK with this.
    return set(my_mapping.values())

f({3: 'yes', 4: 'no'})
```
