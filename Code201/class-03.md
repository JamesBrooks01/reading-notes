# Reading Assignment 03

## HTML

---

### Lists

- In HTML List come in three types
  - Ordered
    - Ordered Lists are created with the `<ol>` element and are listed in numbers.
  - Unordered
    - Unordered lists are created with the `<ul>` element and are listed in bullet points.
  - Definition
    - Definition lists are created with the `<dl>` element and are typically used for terms and their meanings.
- A list can be nested inside of another list, browsers will typically change the style of the list item mark.

### Boxes

- CSS treats each HTML element as if it was contained within a box. CSS is used to manipulate how the box and what is within it is displayed.
- Three of the basic ways to manipulate these boxes are by changing the;
  - Margin
    - The margin sits outside the box and is used to set the distance between borders.
  - Border
    - The border sits on the edge of the box and is used to create a distance from the edges of the box.
  - Padding
    - Padding is the is the distance between the content of the box and the border
  - Balancing these three properly can increase the readability of the contents.
- Using CSS you can also hide elements with the `display` or `visibility` property.
- Elements can be block level, or inline level and using CSS you can set which one you want a box to be.
- By controlling the width of a box, you can increase the readability of a box.
- In CSS3, you can also have image borders and rounded borders.

## JavaScript

---

### Basic JavaScript Instructions

- Arrays are a special kind of variable used to store a list of related information that can be called from for use or later change.
- You create an array much the same as any other variable.
  - You start with a variable keyword, `let` or `const`
  - You give the array a name
  - Then you assign it the values it contains seperated by commas
    - The data within an array don't have to be the same data type, it can be three values, one a `number`, another a `string` and the last a `boolean`.
  - There are two different way to declare an array, either with array literal or array constructor.
    - Array literal is perfered.
    - `let arrayLiteral; arrayLiteral = [1, 2, 3];` is Array Literal
    - `let arrayConstruct = new Array(1, 2, 3);` is Array Constructor
- Values in arrays are organized as if in a list. It is important to know what number the value you need is, other wise you might draw the wrong data.
  - Values in an array start at 0, rather than 1.
    - So, to access the third value in an array you would use the command `let value3; value3 = arrayLiteral[2]` rather than `let value3; value3 = arrayLiteral[3]`.
- Each array also contains the `length` property which defines how many values are stored in the array.
- The values in an array can also be changed with an assignment operator and calling which value you wish to be changed.

### Decisions and Loops

- A switch statement is a different kind of loop that differs from an if-else loop.
  - A switch loop requires a `switch value` and then a list of possible values this variable could be, with a set of code to be run if one of the `"cases"` is true with a `break` keyword to exit the switch statement after running the relevent `case`. It also provides a default set of code if none of the `case`'s return true.
  - The entire statement lives within one set of curly braces `{}` and a colon `:` seperating the options from the statements to be run.
- A switch statement has the advantage over a a series of if statements in that it will only run the relevent code block, where a series of if satements will run one by one even if a match is found.
- Data types can be coerced by the code automatically unless they are compare with a `strict` comparison operator, without strictly compaing them, the coercian can cause unexpected results when comparing data types.
- All values will are evaluated as truthy or falsy
  - Falsy values are things like;
    - `false` boolean
    - `0` number zero
    - `' '` an empty value
    - `1/'value'` (`NaN`)not a number
    - `variable` a variable with no value
  - Truthy values are things like;
    - `true` boolean
    - `34` number's other than zero
    - `string` strings with content
    - `7/5` number calculations
    - `'true'` true as a string
    - `'0'` zero as a string
    - `'false'` false as a string
- The tree types of loops are `for`, `while`, and `do/while`.
  - If a code needs to run a set number of times, use a `for` loop
  - If a code needs to run an unknown number of times, use a `while` loop
  - A `do/while` loop is similar to a while loop except it it will always run the code within at least once, even if the condition evaluates false.
