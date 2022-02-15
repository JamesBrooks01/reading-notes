# Reading Assignment 07

## Domain Modeling

---

- Domain Modeling is he proces of creating a conceptual model for a specific problem. It describes the different entities, attributes and behaviors as well as what constraints have to be worked around.
- A properly articulated domain model can verify the understanding of a specific problem among the various people who have a stake in the success of the code. As a tool, it can define the vocabulary that is used between the technical and business teams.
- Some common practices are;
  - When modeling a single problem that will have many calculations or instances, build sef-contained objects with the same attributes so they can be reused easily.
  - Model the attributes with a constructer function
  - Model the behaviors with small methods that focus on doing one thing well
  - Create the instances with `new` follows by the call to the constructor function
  - Store the new object as a variable so the properties and methods can be used from `outside`
  - Use `this` within methods so the properties and methods can be used from `inside`

## HTML

---

### Tables

- Tables represent data in a grid format. for example, a TV schedule or sports results.
- Tables are composed of 4 main elements.
  - `<table>`
    - Used to create a table with the contents being written out row by row
  - `<tr>`
    - Indicates the start of a row and then closes the row
  - `<td>`
    - Each cell in a row
  -`<th>`
    - Indicates the heading of a row or column. It is good practice to have one even if a cell has no content to represent an empty cell.
    - It can be used with the `scope` attribute to define if it is a heading for the row or column.
- You can if needed make cells of a table span more than one row or column using the `rowspan` or `colspan` attributes.
- For long tables, it is recommended to split the table into a `<thead>`, `<tbody` and `<tfoot>`.

## JavaScript

---

### Functions, Methods and Objects

#### Constructor Notation

---

- The `new` keyword and object constructor create a blank object which can then be added on to with properties and methods.
- To create an object with constructor notation, you use the `new` keyword and `Object()` function. Once created, properties and methods can be added using `dot notation`.
- To then delete a property, the `delete` keyword is used.
- If you want to create multiple objects that represent similar things, object constructors can use a function as a template for creation.
  - When using a template, use the `this` keyword to allow the functions within to work no matter the name of the object.
  - If creating a template with established properties, the values of the properties are provided as parameters for the template.
  - Each statement that creates a property will end with a semicolon instead of a comma.
  - The name of a constructor function often starts with a capital rather than a lowercase.
- To create furthur instances of a template object, the `new` keyword is used infront of the name of the template object.
  - `let testObject = new objectTest (parameter1,parameter2,)`
  - Each time the function is called, the arguments will likely be different.

#### Arrays

---

- Arrays are actually a type of object that hold a related set of key value pairs like all objects, but the key for each value is the index number.
- You can also combine arrays and objects to create complex data structures, for example, an array can hold a series of objects, but be careful to remember the order.
- Or Objects can hold arrays as values of a property.

#### Objects

---

- There are three groups of `Built-In JavaScript Objects`.
  - `Browser Object Model`(BOM)
    - The `BOM` creates a model of a browser tab or window which is top-down,
      - `Window`: Current Browser Window or Tab
      - `Document`: Current Web Page
      - `History`: Pages in  Browsing History
      - `Location`: URL of Current Page
      - `Navigator`: Information about Browser
      - `Screen`: Devices Display Information
    - For example, the `screen` object's `width` property would let you find out he pixel width of the sevice screen.
  - `Document Object Model`(DOM)
    - The `DOM` creates a model of the current web page. It composes everything on the page starting with the `document` object. Some common child objects would be;
      - `<html>`
      - `<head>`
      - `<body>`
      - `<p>`
    - For example, the `document` objects `lastModified` property would detail what date the page was last updated.
  - `Global JavaScript Objects`(GJO)
    - `GJO` doesn't form a single model, they are instead a group of objects that relate to different parts of JavaScript.
    - The names of the objects usually start with a capital letter.
    - The six most important ones are;
      - `String`
        - For string values
      - `Number`
        - For number values
      - `Boolean`
        - For boolean values
      - `Date`
        - To represent and handle dates
      - `Math`
      - To handle mathmatical calculations
      - `RegEx`
        - For matching patterns within text.
    - For example, the `String` objects `.toLowerCase()` method would convert all letters within a variable lowercase.
- To work with dates, you need to create an instance of the `Date` object and then specify the time and date it should represent.
- To create a `Date` object, you use the `Date()` object constructor.  It by default stores the current date and time so if you want it to hold a different date it must be expicitly specified.
- When creating a `Date` object as a variable, it is actually holding a number, specifically the number of miliseconds since midnight on January 1st, 1970.