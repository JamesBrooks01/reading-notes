# Reading Assignment 01

## Introduction to React and Components

---

### Component-Based Architecture

---

- What is a “component”?
  - A component is a set of well-defined functionality that encapsulates the implementation and exports it as a higher level interface and iss modular, portable, replaceable, and reusable.
  - It is also an object that is intended to interact with other componets, encapsulate functiionality or a set of functionality. It has a defined interface and as recommended behavior that is common to all the comnents within an architecture.
  - An object can be defined as a unit that is composed of a specifid interface and explicit context dependencies only. That is to say, It can be deployed independently and is subject to the composition of third parties.
  - A component has three views;
    - Object Oriented
      - A set of one or more classes with each problem domain class and infrastructire class used to identify the attributes and operations that apply to the implementaiton and also defines the interface that enable the classes to communicate and cooperate.
    - Conventional
      - A functional element or module that integrates the processing logic and internal data structures that are required to implement the logic and the interface that allows it to be invoked and the data passed to it.
    - Process-Related
      - In this view, instead of creating each component, it builds from existing components that are maintained in a library. As the architecture is formed, the components are selected from the library and populate the architecture.
- What are the characteristics of a component?
  - Components are;
    - Reusable
    - Replaceable
    - Not Context Specific
    - Extensible
    - Encapsulated
    - Independent
- What are the advantages of using component-based architecture?
  - The advantages of it are;
    - Its easy to deploy it
    - The cost is reduced
    - The development is easier
    - Its reuseable
    - It is a modification of the technical complexity
    - It's reliable
    - The system has easier maintenence and evolution
    - Its independent

### What is Props and How to Use it in React

---

- What is “props” short for?
  - Props is short for Properties and is used to pass data between components.
  - It only flows downwards, from parent to child and is read-only
- How are props used in React?
  - To use props;
    - You define the attribue and the value it has
    - Pass it to the child component
    - Render the data
- What is the flow of props?
  - Props flows downwards to child elements and it is passed like arguments to a function.

## Things I want to know more about

---

- The only question I can really come up with is how this actually saves time, because as much as it say it does, I'm not seeing how this works as an improvement over the way we've been doing it.
