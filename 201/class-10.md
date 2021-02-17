# Class 10

## Error Handling and Debugging

### Order of Execution

- To find the source of an error, it helps to know how scripts are processed. The order in which statements are executed can be complex; some tasks cannot complete until another statement or function ahs been run

### Execution Contexts

- The JavaScript interpreter uses the concept of __execution contexts__. There is one global execution context; plus, each function creates a new execution context. They correspond to variable scope.

### The stack

- The JavaScript interpreter processes one line of code at a time. When a statement needs data rom another function, it stacks (or piles) the new function on top of the current task.

### Execution context & hoisting

- Each time a script enters a new execution context, there are two phases of activity:

  1. prepare - the new scope is created (variables, functions, and arguments)

  1. execute - now it can assign values to variables, reference functions and run their code, execute statements.

### Understanding Scope

- In the interpreter, each execution context has its own variables object. it holds the variables, functinos, and parameters available within it. Each execution context can also access its parents variables object.

### Understanding Errors

- If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code.

### Error Objects

- Error objects can help you find where your mistakes are and browsers have tools to help you read them.

### How to deal with errors

- Now that you know what an error is and how the browser treats them, there are two things you can do with the errors.

  1. Debug the script to fix errors

  1. Handle errors gracefully

### A debugging workflow

- Debugging is about deduction: eliminating potential causes of an error. Here is a workflow for techniques you will meet over the next 20 pages. Try to narrow down where the problem might be, then lookk for clues.(p. 463)

- The js console will tell you when there is a problem with a script, where to look for the problem, and what kind of issue it seems to be.

- The js console is just one of several dev tools that are found in all modern browsers.

- Browsers that have a console have a console object, which has several methods that your script can use to display data in the console. The object is documented in the console API.

#### Breakpoints

- You can pause the execution of a script on any line using breakpoints. Then you can check the values stored in variables at that point in time.

- If you set multiple breakpoints, you can step through them one by one to see where values change and a problem might occur.

- you can indicate that a breakpoint should be triggered only if a condition that you specify is met. The condition can use existing variables.

#### Handling exceptions

- If you know your code might fail, use `try`, `catch`, and `finally`. Each one is given its own code block.

```javascript
try {
  // try to execute this code
} catch (exception) {
  // if there is an exception, run this code
} finally {
  // this always gets executed
}
```

### Throwing errors

- If you know something might cause a problem for your script, you can generate your own errors before the interpreter creates them.

### Debugging tims

- Here are a selection of practical tips that you can try to use when debugging your scripts. (list of common errors p. 485)

### Summary

- if you understand execution contexts (which have two stages) and stacks, you are more likely to find the error in your code.

- Debugging is the process of finding errors. It involves a process of deduction.

- The console helps narrow down the area in which the error is located, so you can try to find the exact error.

- JS has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.

If you know that you may get an error, you can handle it gracefully using the try, catch, finally statements. use them to give your users helpful feedback.

[back to README](README.md)
