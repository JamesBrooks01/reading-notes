# Reading Assignment 07

## Ten Thousand 2

---

### Python Scope

---

- Python resolves names using the LEGB rule, named for thr Python scope for names meaning Local, Enclosing, Global, and Built-In.
  - Local is the code block or body of any Python Function or Lambda Expression. It contains all the names defined within the function and will only be visible from the code. It is created at call, not definition so you'll have as many local scopes as you do function calls. This is true even for calling the same function multiple times and even recursively.
  - Enclosing or nonlocal scope only exists for nested functions where if the local scope is an inner or nested ucntion then the enclosing scope is the scope of the outer function. It contains the names defined in the enclosing function and are visible from the inner and outer scope.
  - Global or module scope is the top-most scope in a program, script, or module. It contains all the names declared at the top level and are visible from anywhere.
  - Built-In scope is a special scope that exists when you run a script or open an interactive session. It has the keywords, functions, exceptions and other Python native attributes. They are also availible from anwhere in the code.
- This LEGB rule defines the order that Python looks up names where it returns the first occurrence of the word, otherwise returning an error.
- NonLocal Scope is the scope for nested functions and takes the form of the local scope of the enclosing function's local scope.
  - All the names defined in the enclosing function before the nested function are available to the inner function.
  - You cannot modify any names that exist in the enclosing scope from the inner scope unless you declare them `nonlocal` within the nested function.
- Global Scope is the top-most scope and when you first start a Python Program you are in the global scope.
  - On an internal level, Python turns the main script into a `__main__` module that holds the main program execution and the namespace of this module is the global scope of the program.
  - If you want to see all the names that exist in the global scope, use the `dir()` method without arguments.
  - There is only one global scope per program and exists until the program terminates and all names are forgotten.
  - You cannot assign global names within a function unless using a `global` statement.
  - If you assign a name that matches a global name within a function, the local scope name will take priority within the function.
- You can modify the behavior of a Python scope, specifically the Global and NonLocal Scope.
  - You can modify the behavior of Global Scope with the `global` statement.
    - By using this statement you are defining a list of names that are to be treated as global names and is made of the `global` keyword followed by comma seperated names.
    - It should be noted that the use of the `global` statement is considered bad practice and it is better to write self-contained functions that rely on local names rather than modifying global ones.
  - You can also modify the behavior of NonLocal Scope with the `nonlocal` statement.
    - In a similar fashion to global names, nonlocal names can be accesed by inner functions but not assigned or updated and to modify them requires the `nonlocal` statement written the same as the global statement.
    - In contrast to `global` you cannot define names that don't already exist in the outer function.

### Don’t be Confused by Big O Notation Anymore

---

- Big O notation is a way of defining the run-time of an algorithm. It defines the rate of growth when you give it increasingly large amounts of data.
  - O(1) is constant time unit, no matter the size of the input, it always takes the same amount of time.
  - O(log n) is logarithmic, and is likely the best scaling other than O(1) as it slows down in growth the larger the input.
  - O(n) is linear time growth where the time it takes to output grows as the size of the input does.
  - O(n logn) is Log-Linear growth where it grows faster than linear
  - O(n^2) is polynomial growth that grows even faster than Log-Linear and increases in rate as the input increses.
  - And O(x^n) is Exponential growth which the rate of growth increases extremely rapidly as the size of the input increases.