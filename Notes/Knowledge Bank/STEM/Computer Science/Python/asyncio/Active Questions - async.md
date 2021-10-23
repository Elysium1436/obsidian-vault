1. How the hell can [[Futures]] tell the event loop that it's ready, when the execution of the program is on another task? How can the [[Futures]] flip a switch when it can't even do anything? How can it, for example, receive a request that it has been waiting when it doesn't has control? 
	- We learned that only a `Future` object can pause the execution flow. We also learned that we can check if the `Future` object is done by calling it's `.done()` method. But again, how the hell can it flip the switch when the execution isn't even on it? Even if the switch flips only when the loop checks on it, how the hell does the future completes whatever io operation it does? How the hell can it receive a request even without thread paying attention to the socket? ffs -_- 
	- Perhaps this is just related to "how can we create a future". Searching that may prove useful.
2. How exactly do you create the baseline awaitable code? Like, how do you make a request function awaitable? How do you pass the execution flow? So far i've seen using the await statement on already in-built stuff, that abstracts away the waiting part, but I still have no clue on how to actually build these types of awaitable functions, where I have an IO bound function, and I can yield the execution flow while waiting for the io operation to complete.