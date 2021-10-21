## Executors

Executors are made for blocking functions that are not naturally compatible with asyncio.


To use it, first get the running [[Loop]], then we can create a custom Thread [[Pool]].

```python
import asyncio
import concurrent.futures

async def main():
	loop = asyncio.get_running_loop()
	
	with concurrent.futures.ThreadPoolExecutor() as pool:
		result = await loop.run_in_executor(
			pool, blocking_io)
		
		
asyncio.run(main())
	

```