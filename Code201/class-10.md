# Reading Assignment 10

## JavaScript

---

### Error Handling & Debugging

- JavaScript can be challenging to learn and everyone can make mistakes when writing it, so it's important to know the proper practice for handling errors and how to debug the code. An important thing to understand when dealing with errors or unexpected output is to know how the interpreter processes the code. The interpreter goes one line at a time, left to right and when the code needs data from another function it stacks the needed function on top of the current one, pausing the code until it gets what it needs.
- Another thing to think about and understand is `scope`. Each function has its own variable scope and variables defined within a function only exist within that function and can only be accessed by itself and any children the function has.
- Functions also execute in two stages, preparation where the scope is created and all the variables, functions, and arguments are created, and then execution where it assigns the values, references functions, runs code, and executes statements. Because of this process, certain things that you would think would cause an error like calling a function before it's defined, work because of hoisting.
- When the interpreter generates an error, it throws out an exception and then checks for error handling code, and if it finds none, it generates an error object and stops running. The error object contains multitudes of data that can be read to find out what went wrong and a smart coder can use it to figure out how to fix it. The 4 most common error types to encounter are;
  - Syntax
    - A syntax error is composed of things like missing semicolons, missing brackets, and other similar things.
  - Reference
    - Reference errors are things like variables not existing and undefined functions.
  - Type
    - A type error is something related to values not being the correct data type or the code is trying to use an object or function that doesn't exist.
  - Range
    - A range error is when you call a function whose numbers are outside the accepted range.
- A very helpful tool for debugging javascript is the browser's dev tools page and the javascript console.
  - An easy way to use the JavaScript console is to use a `console.log` or `console.table` on values that might be causing errors or not getting the data you think they should.
    - When using the console logs for debugging it can also be useful to group related logs together with `console.group`.
- Another tool is to put breakpoints in the code to pause the code at certain points.
- If you know your code might fail, you can use the `try`,`catch`, and `finally` code to have the code `try` to run the code, `catch` the error and run an alternative set of code, and `finally` run a code block regardless of the outcome of the `catch`.
- If you think something might cause an issue, you can create a manual error message. For example, if the user inputted a string when you expect a number, then a manual error message will stop the code from resulting in another error down the line that would be harder to track down the cause of.
