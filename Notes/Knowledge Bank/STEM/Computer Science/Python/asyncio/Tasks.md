
### Tasks

Tasks are in general, an element of the event loop, which will execute code in a concurrent fashion. Each one of them contains their own call stack.

One way of creating and using task is to use the `asyncio.create_task()`. To use it, you can either await the tasks, which will execute the tasks in the main event loop concurrently

```python
async def main():
    task1 = asyncio.create_task(
        say_after(1, 'hello'))

    task2 = asyncio.create_task(
        say_after(2, 'world'))

    print(f"started at {time.strftime('%X')}")

    # Wait until both tasks are completed (should take
    # around 2 seconds.)
    await task1
    await task2

    print(f"finished at {time.strftime('%X')}")
	
```

Or you can get the event loop using `asyncio.get_event_loop()`, call it's `.create_task()` method, and call a method to execute the loop.

```python

loop = asyncio.get_event_loop()
t1 = loop.create_task(fetcher())
t2 = loop.create_task(monitor())
loop.run_forever()
#or you can use
loop.run_until_complete()
#If you want to run various awaitable objects concurrently, you can use
L = await asyncio.gather([t1,t2])
#If any object in the iterable is a coroutine, it'll be changed to a task. If you 
```


