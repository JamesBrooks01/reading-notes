# Reading Assignment 09

## Functional Programming

---

### Functional Programming Concepts

---

- What is functional programming?
  - A programming paradigm that trats compuation as the evaluation of mathmatical functions and avoids changing state and mutable data.
- What is a pure function and how do we know if something is a pure function?
  - A pure function is one that always returns the same result if given the same arguments and doesn't cause any observable side effects.
- What are the benefits of a pure function?
  - They are easier to test and they are generally stable, consistent, and predictable with less need for coding in situations with different results given the same input because it won't happen.
- What is immutability?
  - Something whose state cannot be changed. An immutable object that you try and change will instead make a new object with the new value.
- What is Referential transparency?
  - The combination of using pure functions with immutable data.

### Node JS Tutorial for Beginners #6 - Modules and require()

---

- What is a module?
  - A chuck of code that has a specific funtionality that is split off from the main code into it's own .js file.
- What does the word ‘require’ do?
  - It creates a global object to be used within the file it's called in.
- How do we bring another module into the file the we are working in?
  - By using require and the file location.
- What do we have to do to make a module available?
  - By exporting whatever function or code the module contains that you want to use elsewhere.
