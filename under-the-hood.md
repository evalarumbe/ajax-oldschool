# Peek under the hood (skip this for now if it's too much, but in case you're curious...)

This 30 min video is an entertaining and informative peek under the hood. https://www.youtube.com/watch?v=8aGhZQkoFbQ

Here's a summary of the video.

JavaScript is single-threaded, but the environment (in this case, the browser) provides a system to achieve concurrency. This includes:
- another thread - for parallel processing (handling many instructions at once)
- a task queue - a to-do list of instructions 
- an event loop - to decide when to retrieve things from the task queue.

The task queue receives all the instructions, synchronous and asynchronous, to keep track of when they should be carried out.

The event loop repeats the following steps continuously:
- check if the call stack is empty. When it is, then:
- shift the next item from the task queue and process it