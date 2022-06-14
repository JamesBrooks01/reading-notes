# Reading Assignment 42

## Pythonisms

---

### Dunder Methods

- Dunder Methods are a set of pre-defined methods that start and end with double underscores.
- They got the name Dunder as to mean double-under.
- Dunder methods allow the emulation of the behavior of built-in types like the length attribute of a string or slice syntax.
- The design is referred to as the Python Data Model and can be thought of as an API that an be interfaced with by using one or more of these Dunder Methods.
- The 7 types of Dunder Methods listed in the article are;
  - Object Initialization(`__init__`)
    - Class Constructor Method
  - Object Representation(`__str__`,`__repr__`)
    - It is common practice to include a string representation which can be done with either;
      - `repr` for the "official" string and is supposed to be unambiguous.
      - `str` for the nicely printable string version.
  - Iteration(`__len__`,`__getitem__`,`__reversed__`)
    - `len` returns a number representative of how many of a specific attribute there is, such as the number of transactions in an Account class or the number of nodes in a Linked List
    - `getitem` allows you to return an item at a specific position in the class, allowing iteration as well.
    - If you want to iterate in reverse order, you also need the `reversed` dunder method.
  - Operator Overloading for Comparison(`__eq__`,`__lt__`)
    - When making comparisons, there are several dunder methods at work and when building your own if you don't want to implement all of them, you can use total_ordering from functools to only need to implement `eq` and `lt`.
    - `eq` for equals and `lt` for less than.
    - With those two, you can also handle their opposites due to the way they are implemented.
  - Operator Overloading for Merging(`__add__`)
    - To merge two of the same object together, it uses the `add` dunder and can be specified to add them together however you wish.
  - Callable Python Objects(`__call__`)
    - You can also make the object callable like a regular function with the `call` dunder. However, the major issue with it is knowing what the purpose of calling the object would be and therefore it is more common to make a method on the class that is named what you would want to return instead.
  - Context Manager and With Statement(`__enter__`,`__exit__`)
    - A context manager is a protocol that the object needs so it can be used with the `with` statement.
    - To use it, you need the `enter` and `exit` dunders.

---

### Iterators

- The most basic dunder method for adding iteration is `iter`.
- In the example they also have a helper-class that is returned that when combined allows for a for-in loop to run on the class returning something.
  - However, without something that indicates the end, it will iterate forever.
- Expanding the for-in loop reveals that it is a simple while loop that prepares the object by calling the `iter` method and then repeatedly calls the `next` method to retrieve values from it.
- The use of an iterator allows us to process every element of a container while remaining isolated from the internal structure.
- Regardless of the data structure, each type is an implementation detail to it because each one can be traversed with the power of iterators.
- In the initial example the work was split into two classes but often both of them can be in a single class.
- Now, to implement a way for the iteration to know where to stop.
  - The easiest is to implement a pre-defined number of repetitions.
  - The iterators use a StopIteration exception to stop iteration when they run out of elements.
- One main difference in this case between Python 2 and 3 is that in 2 it is simply `next` with no underscores whereas in 3 it has the underscores; `__next__`.
- In summary,
  - Iterators provide a sequence interface that is pythonic and memory efficient.
  - To support iteration, it needs the `iter` and `next` dunder methods.
  - Class-based iterators are only one way to write iterable objects, there are also generators and generator expressions.

---

### Generators

- Generators are a shorter way of writing iterators.
- They use the `yield` statement instead of `return`
- The code in the generator function only runs when `next` is called on the generator object.
- One thing to understand about the `yield` keyword is that unlike `return` which passes all control back to the caller, `yield` only does so temporarily.
- Another way of thinking about it is that `return` disposes of the local state, `yield` suspends the function and retains the local state.
- When using the `yield` statement, it stops generating values when control is returned to the caller through any means other than a `yield` statement.
- Using generators allows you to abstract away much of the boilerplate code that is needed for class-based iterators.
- In summary,
  - The `yield` statement allows for the temporary suspension of the execution for the generator function and pass values back from it.
  - Generators start raising StopIteration exceptions when the control flow leaves the function by anything other than a yield statement.
