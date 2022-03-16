# Reading Assignment 03

## Passing Functions as Props

---

### React Docs - lists and keys

---

- What does .map() return?
  - An array.
- If I want to loop through an array and display each value in JSX, how do I do that in React?
  - By using the .map() method, and assigning the array it returns an element that is rendered in the DOM.
- Each list item needs a unique ____.
  - A key.
- What is the purpose of a key?
  - They help React identify when items change, are added or removed.

### The Spread Operator

---

- What is the spread operator?
  - The spread operator is a quick way to add items to an array, combine an array or object and to spread an array into a function's arguments.
- List 4 things that the spread operator can do.
  - Copy an Array
  - Use Math Functions
  - Use an Array as Arguments
  - Combine an object
- Give an example of using the spread operator to combine two arrays.
  - `let array3 = [...array1,...array2]`
- Give an example of using the spread operator to add a new item to an array.
  - `let array2 = ['1','2',...array1]`
- Give an example of using the spread operator to combine two objects into one.
  - `let object3 = [...object1,...object2, property1: "1"]`

### How to Pass Functions Between Components

---

- In the video, what is the first step that the developer does to pass functions between components?
  - Create the funtion in the parent component.
- In your own words, what does the increment function do?
  - When called it runs through an array and matchs the name of the component it was called from to the correct component in the array and increments the count property by 1.
- How can you pass a method from a parent component into a child component?
  - As a prop that contains the method.
- How does the child component invoke a method that was passed to it from a parent component?
- After passing the method as a prop, you call it in a function that the child uses.
