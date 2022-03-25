# Reading Assignment 10

## In Memory Storage

---

### Understanding the JavaScript Call Stack

---

- What is a ‘call’?
  - A function invocation
- How many ‘calls’ can happen at once?
  - Only one call can happen at a time.
- What does LIFO mean?
  - Last In, First Out. As in the last function to be called is the first to return when the stack resolves.
- Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
  > function1() {<br>
  > console.log(call stack)<br>
  >}<br>
  >
  >function2() {<br>
  > function1()<br>
  >}<br>
  >
  >function3() {<br>
  > function2()<br>
  >}<br>


- What causes a Stack Overflow?
  - When a function that calls itself reaches the maximum stack call number that the browser allows.

### JavaScript error messages

---

- What is a ‘refrence error’?
  - A variable that is not yet declared or if you access a let or const variable in the TDZ.
- What is a ‘syntax error’?
 - When something cannot be parsed syntactically.
- What is a ‘range error’?
  - Trying to manipulate an object with a length and you give it an invalid length.
- What is a ‘tyep error’?
  - When trying to use or access data that has an incompatible data type.
- What is a breakpoint?
  - A line of code you want to stop the code at, often for debugging purposes.
- What does the word ‘debugger’ do in your code?
  - Sets a conditional for a line of code to run.
