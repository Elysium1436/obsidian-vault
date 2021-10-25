### Typing Basics

Typing is used on function arguments, like this
```python
def greeting(name: str) -> str:
    return 'Hello ' + name
```

Here is a list of the non-obvious Stuff
> ```python
> from typing import Iterable, Union, Optional, Callable, List, Any
> def f(num1: int, my_float: float = 3.5) -> float:
>       return num1+ my_float
>  x: Callable\[\[int,float\]\]
> ```