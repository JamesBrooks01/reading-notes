# Reading Assignment 02

## HTML

---

### Text

- HTML Elements come it two types, Structural and Semantic
  - Structural Elements define the structure of a page,
    - What text is in the Heading
    - What text is a paragraph
    - What text should be bolded or italicized
    - If there is any Superscript or Subscript
    - Inserting line breaks or horizontal breaks
  - Semantic Elements don't change the structure of the web page, only provide more information.
    - Setting text as 'Strong' or 'Emphasized'
    - Adding in quotations as either a blockquote or regular quote
    - Add in a definition of an abbreviation or acronym
    - Insert Citations or Definitions
    - An address, digital or physical
    - Putting a Strikethrough on text

### Introducing CSS

- To fully understand CSS, think of each element as being a box that can be manipulated.
- CSS sets rules for these boxes that change how each box and its contents are shown on the Web Page
- Rules are formed of two pieces,
  - The Selector
    - Defines what element type will be affected
  - The Declaration
    - Defines how it will be changed.
    - Is made of a property and a value
      - The property indicates what part of the element will be changed(size,color,border,etc.)
      - The value sets what the property will be set to.(Red text, 14px font size,etc)
- CSS rules can be indicated within the HTML document but are usually contained within its own document.
- CSS rules follow the priority of "External < Internal < Inline"
  - The external document sets the rules, but the internal rules can overwrite it, and the inline rules will always take priority of display.

## JavaScript

### Basic JavaScript Instructions

- JavaScript is essentially a series of instructions for the computer to follow using variables to store information.
- Variables have to be declared before they can be used. To declare a variable requires,
  - A variable keyword
    - There exist three keywords, var, let, and const.
      - `var` is the old way of declaring variables
      - `let` is for a variable that is changeable
      - `const` is for a static or unchanging variable
  - A variable name
    - The name can be anything, but if it is more than one word it follows the format of camelCase where the first word is lowercase and any subsequent words have the first letter capitalized.
- Once a variable has been created, it must be assigned a value with an equals(=) sign otherwise known as an assignment operator.
- The series of instructions that the Script follows is very precise, the value of a variable has to be created and assigned before it can be used in any calculations.
- Using an Array, you can store multiple pieces of related information
- JavaScript has a distinction in the types of information, and in certain cases the type of data can matter.
  - The data can be a number(0-9), a String('Hello World'), or a Boolean value(`true` or `false`)
- A JavaScript expression relies on operators to make it's calculations and all of them will end or return a single value.

### Decisions and Loops

- In JavaScript code, there are often places where a decision has to be made about the data you have, this is used to have one set of instructions run instead of another. To make this decision, you set your desired condition, whether that is two values being equal, one greater than the other or less than the other. If the condition is `true`, you run one of the paths, `false`, you run the other.
  - This type of evaluation is typically done using an `if/then/else` statement where `if` the condition returns the desired outcome, `then` run this set of code, `else` run this set(or skip this code entirely).
- Conditional Statements are used to allow the code to make decisions about what code to run or in which order.
- To make comparisons, there are many different operators to use, such as,
  - Equal To(`==`)
  - Equal value and Equal type(`===`)
  - Not Equal(`!=`)
  - Not Equal value or Not Equal type(`!==`)
  - Greater than(`>`)
  - Less than(`<`)
  - Greater than or Equal to(`>=`)
  - Less than or Equal to(`<=`)
- Using Logical Operators, you can combine more than one set of comparisons such as,
  - And (`&&`)
  - Or (`||`)
  - Not (`!`)
  