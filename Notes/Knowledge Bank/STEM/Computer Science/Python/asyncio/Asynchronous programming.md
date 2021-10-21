### Asyncronous programming

Normally, when we are programming, we use the "Stacks and Frames" framework. In this method, each function creates a frame on the "stack machine". It allows us to call a piece of code from another. Each level of nested calls increases the height of the stack with a frame. Each frame has it's own scope of values, and the position of what line to return when the frame above returns a value.

When using async programming though, we use what is called an event loop. An event loop is simply a list of [[Tasks]]. Each [[Tasks]] has it's own stack, and it's own execution pointer.

Since in a single-threaded environment we can only have one task executing at a given time, every other task remains paused until the active task yields it's execution pointer.

The task will execute just like a syncronous function up until it encounters a point where it has to wait again. Then it proceeds to give control back to the event loop, and wake it up again at a future point once whatever it was waiting on has happened.

The currently executing [[Task]] cannot be paused by any means other than awaiting a [[Future]], or an object that behaves like one. Any `await` statement *might* cause the Task to pause, but that's not guaranteed. Any statement that is *not* an `await` statement *cannot* make the current Task pause.

![[Pasted image 20211017163310.png]]



#### References
https://bbc.github.io/cloudfit-public-docs/asyncio/asyncio-part-1