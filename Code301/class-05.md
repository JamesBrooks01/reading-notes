# Reading Assignment 05

## Putting it all together

---

### React Docs - Thinking in React

---

- What is the single responsibility principle and how does it apply to components?
  - The idea that each component should only do one thing and the more it grows beyond, the more subcomponents it should have.
- What does it mean to build a ‘static’ version of your application?
  - A version that has no iteractivity, everything is passed as props with no state.
- Once you have a static application, what do you need to add?
  - State to make it iteractive.
- What are the three questions you can ask to determine if something is state?
  - Is it passed via props?, Does it remain unchanged?, Can it be computed based on another state or prop?
- How can you identify where state needs to live?
  - A common parent component or another component higher up the hiererarchy.

### Higher-Order Functions

---

- What is a “higher-order function”?
  - A function that operates on other functions either by returning them or using them as arguments.
- Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
  - Returning true or false based on if the parameter is less than m.
- Explain how either map or reduce operates, with regards to higher-order functions.
  - Map applies a function to every element in an array and returns a new array based on the result.
