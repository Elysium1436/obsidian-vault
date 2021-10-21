### Event Loops

To get the current event loop, use:
```python
loop = asyncio.get_event_loop()
```
To schedule a task into the event loop, use:
```python
t = loop.create_task(couroutine_function())
```
There are various ways to run the event loop. below is a comment from [this stack overflow question.](https://stackoverflow.com/questions/50592540/asyncio-create-task-to-run-forever)

>The argument to run_until_complete controls how long the event loop is run. And once the event loop stops running, all coroutines are effectively suspended, not just the one that you've been waiting for. But you do have different options:
>- `loop.run_until_complete(some_func())` - what you already used; run the event loop until the some_func coroutine finishes. Executes other coroutines in parallel during that time as well, but also stops executing them as soon as the event loop finishes.
>- `loop.run_forever()` - run the event loop until some coroutine or callback invokes `loop.stop()`. If none of them do that, then the event loop will not halt, even if all the coroutines come to an end. In your case you'd call `loop.create_task(while_loop())` followed by `loop.create_task(some_func())` and then `loop.run_forever()`.
>- `loop.run_until_complete(asyncio.gather(while_loop(), some_func()))` run the event loop until both the specified coroutines finish. This (wait for all the tasks) is apparently what you expected `loop.run_until_complete()` to do automatically even if you name only one, except it doesn't work like that, it stops as soon as the specified coroutine finishes. `asyncio.gather` can be used to wait for multiple coroutines at once. For a more fine-tuned control of waiting, also see `asyncio.wait`.