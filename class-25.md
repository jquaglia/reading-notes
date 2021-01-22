# Class 10

## Call Stack

A call stack is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions.

- when a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

- any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

- when the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

- if the stack takes up more space than it had assigned to it, it reults in a "stack overflow" error.

- in Asynchronous JavaScript, we have callback function, an event loop, and a task queue.

- LIFO: last in, first out
