# Reading Assignment 04

## Readings: Topic

---

### Classes and Objects

---

- An object in Python is an group of variables and functions contained into a single entity. Objects get variables and functions from classes and Classes are a template to create objects.
- To assign a Class to an Object you use the syntax of `python_object = class_name()`.
- To access a variable within an Object you use the syntax of `python_object.variable_name`.
- You can create multiple Objects that are the same Class with each Object containing their own copies of the variables defined within.
- To access a function, you use a similar syntax to a variable; `python_object.function_name()`.
  - There is a special function called `__init__()` that is called when the class is initiated and is used for assigning the values in a class.

### Thinking Recursively

---

- Some problems in coding may at first seem big and challenging, but by breaking it down into smaller easier to solve chunks the bigger issue will turn out to be easier to solve than you thought.
  - This thinking is the core idea behind recursive thinking.
- The core idea behind a recursive algorithm is that if a problem is simple, solve it and if not divide into smaller sub-problems and apply the same strategy.
- Now, to be more specific to Python, a recursive function is a function that either directly or indirectly calls itself within it's function and continue to repeat until a condition is met and the result is returned.
- When dealing with a recursive function you have to maintain the state which can be achieved by either;
  - Threading the state through each call so the current state is part of the call's context
  - Or, keep the state in a global scope
- A data structure can be described as recursive if it can be defined in terms of a smaller version of itself. A list is one example.
- When used together, a recursive function's structure can often be modeled after the definition of the recursive data structure it uses as an input.

### Pytest Fixtures and Coverage

---

- When writing test for code it is rare to only write one or two, it is much more common to write a wide variety of tests to check a different potential path through the code.
- In many cases there will be test that have similar characteristic that can be handled with parametrized tests, but in other cases you'll need some objects be available to all the test and they might contain data that you want to carry over to other tests and for those you use a fixture.
- A fixture is defined with the `pytest.fixture` decorator and a function definition.
  - Fixtures appear and in some senses act like a global variable in that you pass the function name as a parameter without parentheses but is still a function that gets executed everytime a test is executed with it as a parameter.
  - You can also control the scope of fixture to control how often it runs, such as setting it to module where it will run once and then keep the data availabe to any other tests that use it.
- Using the package `pytest-cov` you can invoke pytest with the `--cov` option that will give a coverage report on any function you give it or all of them if you don't.
  - To make it human readable you use `coverage html` which creates a htmlcov directory containing a file that opens in the browser and gives a report of all the areas the function lacks coverage.
