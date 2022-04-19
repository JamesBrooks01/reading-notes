# Reading Assignment 02

## Testing and Modules

---

### In Tests We Trust — TDD with Python

---

- Unit Tests are pieces of code to test the input, output and behavior of code. They can be written anytime but Test-Driven Development is the strategy of writing the tests first.
- The idea of writing tests first is to think of what the client needs and how to test the code to ensure the answer you get is the one you want before writing out the code that will do it.
- When writing test code there are some important aspects to remember.
  - Ensuring the Test Name is descriptive of what the test is and what it expects to recieve.
  - Ensuring the Module Name matches the file/module that it is testing. So name.py would be named test_name.py.
  - Another good practice is to keep the tests in a seperete tests directory.
  - The commonly used structure for tests is AAA, or;\
    - Arrange
      - Organizing the data needed to execute the code(Input).
    - Act
      - Execute the code being tested
    - Assert
      - After executing the code, checking the result(Output) and ensuring it is what you were expecting.
  - The next important thing to use is the cycle.
    - Write the test and ensure it fails as the feature it tests isn't there yet
    - Write the feature and ensure it passes the test
    - Refactor the code to make it neater
  - An advantage to TDD is that it forces us to think about the design first and how it can be broken into smaller pieces.

### If name equals main

---

- When Python executes code, it first reads the source file and defines a few special variables. If the interpreter is running the module(source) as the main program it will set the `__name__` variable to `__main__`. If the file is being imported it will be named to the module name.
- When the fiie is executed as a command, it will execute all the code at indentation 0, Functions and Classes are defined but none of the containing code is run.
- In the example they provide they have a section of code under the if statement of `if __name__ == __main__`. This allows certain blocks of code to only run if it is being run directly or as a module.
- The advantage to this is that each module has a `__name__` variable and if it is set to `__main__` then it implies that the module is being run as a standalone and the code can perform the appropriate actions.
- Python files can be either a reusable modle or a standalone program.

### Recursion

---

- Recursion is the process where a function calls itself directly or indirectly. One advantage of using a Recursive Algorithm is that certain problmems can be easily solved.
- An example of this is the problem of determining the sum of the first `n` natural numbers. There are many ways to do this but the simplest is to simpy add all the numbers from one until n.
- With a recursive algorithm, the function doing the calculation is called within itself to continue to calculate until the base condition is fufilled.
- The base condition is essentially what the smallest solution to the problem is with the rest of the calculations being handled by the function.
- The idea of using recursion is to represent the bigger problem as one or more smaller problems and add one or more base conditions that will stop the recursion when the problem is solved.
- If the function doesn't have a base conditon you will run into a StackOverflow problem which is when the funtion calls itself infinitely without a way to stop itself and it will instead run until the memory it uses runs out.
- Another thing to understand is how to differenciate between direct and indirect recursion.
  - A function recursion is direct if it calls itself within the function, ex. `fun` function calling `fun` within itself.
  - A function recursion is indirect if it calls another function that directly or indirectly calls the previous function. ex. `fun` calling `newFun` which calls `fun` or another layer of recursion further.
- Recrsion can also be further differenctiated by if it is `tailed` or `non-tailed`.
  - A tailed recursion is one where the recursive call is the last thing executed by the function.
- Now, there are some disadvantages to using recursive programming over itertive programming.
  - Both methods have the same problem-solving powers with every function being able to be written with both methods.
  - A recursive program will require more space than an iterative as every function will remain in the stack until the base condition is resolved. It also has a greater time requirement due to function calls and return overhead.
- But, there are also some advantages to recursive programming over iterative programming.
  - Recursion is clean and simple. Some problems are also inherently recursive and thus is is perfered to write the solution recursively.
