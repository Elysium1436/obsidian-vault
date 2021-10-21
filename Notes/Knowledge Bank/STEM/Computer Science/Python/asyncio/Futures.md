### Futures

Future are objects that when *awaited* causes the current Task to be paused until a specific condition occurs. It can be abstracted as some process that is happening elsewhere that can be finished or not. 

It has three important methods:
- `f.done()` which returns `True` if the process has been finished
- `f.exception()` raises an `asyncio.InvalidStateError` exception if the process has not yet finished. If it is finished, it returns the excpetion it raised, or `None` if it terminated without raising.
- `f.result()` raises `asyncio.InvalidStateError` exception if it has not yet finished, raises the exception that the process has raised, or the value the process returned if it finsihed without raising anything.


You can create a future with 
```python
f - asyncio.get_event_loop().create_future()
```
but it is not used unless you are extending the asyncio library.