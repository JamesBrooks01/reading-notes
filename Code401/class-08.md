# Reading Assignment 08

## Ten Thousand 3

---

### List Comprehensions

---

- Considering the number of lists you'll deal with as a Python Programmer, it will serve you well to understand and use Python's more concise methods of handling lists and list comprehension.
- List comprehension is way of creating lists in Python that as you work more with lists and lists within lists becomes more essential.
- An easy example of list comprehension is `new_list = [expression for item in list]`.
  - This list comprehension is composed of three ingredients;
    - The `expression` to be carried out.
    - The object the expression will work on, `item` in this case.
    - The iterable list of objects to build the new list from, `list` in this case.
  - To better understand what this means, think about it as an expression to be performed on each item in the list to create a new list with each item modified by this expression.
  - You can also add conditional statements to allow for more precision in the way you handle lists.
- A method of creating a list of numbers is with `range()`.
  - In list comprehension you can do this with `[x for x in range(10)]`
  - `range()` by itself already can do this, but doing it with list comprehension is a good start to learning the real power of list comprehensions.
- Another, better to show the power of list comprehension is by comparing a way of creating a list with a for loop vs list comprehension.
  - The for loop uses 3 lines of code
    - `squares = []`
    - `for x in range(10)`
      - `squares.append(x**2)`
  - The list comprehension version works in 1 line.
    `squares = [x**2 for x in range(10)]`
- The list of things you can do with List Comprehesions is lengthy but here are some examples;
  - Multiply every element of a list by 3
    - `multiples_of_three = [x*3 for x in range(10)]`
  - Find all the even numbers in a list;
    - `even_numbers = [x for x in range(1,20) if x%2 == 0]`
  - Grab only the first letter of each string in a list of strings;
    - `letters = [name[0] for name in authors]`
  - Seperate each letter in a string into a list element;
    - `letters = [letter for letter in "20,000 Leagues Under The Sea]`
  - Convert each element to upper or lower case
    - `lower_case = [letter.lower() for letter in ["A","B","C","D"]]`
  - Extract all the numbers from a string;
    - `phone_number = [x for x in user_data if x.isdidget()]`
  - Read and parse files;
    - `poem = [line for line in file]`
- You can also use functions in list comprehension to perform a custom action on each element
  - For example a function that doubles any input could be used like;
    - `nums = [double(x) for x in range(1,10)]`
- Hopefully, these examples have been enough to spark creativity for potential things you could accomplish with list comprehension.
