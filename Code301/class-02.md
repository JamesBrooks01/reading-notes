# Reading Assignment 02

## State and Props

---

### React Lifecycle

---

- Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
  - Render
- What is the very first thing to happen in the lifecycle of React?
  - Mounting
- Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
  - Constructor
  - Render
  - componentDidMount
  - React Updates
  - componentWillUnmount
- What does componentDidMount do?
  - It loads anything that uses a network request or initializews the DOM. Such as Subscriptions.

### React State Vs Props

---

- What types of things can you pass in the props?
  - Mostly static data that is passed from a parent element and doesn't change. It can also be thought of like arguments in a function.
- What is the big difference between props and state?
  - Props are passed into a component and States are handled within the Component.
- When do we re-render our application?
  - When the State changes.
- What are some examples of things that we could store in state?
  - Any data that is handled completely within it's own component and can then be passed on such as an imput like a checkbox or a counter.

## Things I want to know more about

---

- What subscription means in this context. I assume it is likely a data point that determines that the person is logged in and to indicate to the code a set of data to display or something like that.
- Due to the way this works, I assume we will be moving on from Local Storage, but I ask if you can even use Local Storage with this?
