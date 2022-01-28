# Programming with JavaScript

## Control Flow

---

Conrol Flow defines the order that the code is run and executed. Code runs in order from line 1 down unless it reaches something that changes the flow, like a conditional or loop.<br>
For Example, a script that validates data given in a webpage form will prompt the user to fill the data in if they leave it empty or they give an invalid input.<br>
A typical script will contain many control structures like conditiionals, loops and functions.<br>
This is why it's important to read the code carefully and pay attention to the program structure and how it affects the order that the code executes in.

## Functions

---

Functions are an easy way to group a block of code together to perform a specific task. A function only executes or runs when something invokes it.

### Syntax

---

JavaScript functions are defined by the `function` key word followed by a **name** and then closed parentheses `()`. A funtion name can include letters, numbers, underscores and dollar signs. <br>
The parentheses may include parameter names seperated by commas. <br>
The code that is to be executed is placed in curly brackets `{}`.<br>
For Example,
>`function testName(testParameter) {
        code
    }`

### Invocation

---

The code inside the function will execute when the function is invokes by,<br>
- An event occuring(like a button being pressed)
- It is invoked directly in the code
- Automatically (Where the function invokes itself)

### Return

---

When a JavaScript encounters a `return` code, the funtion stops and outputs its designed outcome or data if any. Functions will often compute a return value which is then "returned" back to what invoked it. For Example,<br>
>` function mathTest(x, y) {`<br>
`return x + y;`<br> 
`}`<br>

Would `return` the sum of x and y.

### So, Why Functions?

---

Functions allow you to easily resuse code as once you define it in the function once, you can invoke the function as many times as you want and it will run each time. If you give the function a dynamic input, the `return` value could be different each time.

## JavaScript Operators

---

JavaScript has many different types of operators that each handle the data differently. The main ones are,<br>
- Arithmatic
    - Used to Perfrom Arithmatic on Numbers
        - Addition(`+`)
        - Subtraction(`-`)
        - Multiplication(`*`)
        - Exponentiation(`**`)
        - Division(`/`)
        - Increment(`++`)
        - Decrement(`--`)
- Assignment
    - Assigns values to Variables, and can perform the Arithmatic with the two variables
- String
    - `+` adds two strings together
        - `text1 = text2 + " " + text3` Would result in "text2 text3"
        - `name = John + " " + Doe` Would become "John Doe"
- Comparison
    - Compares two numbers with each other
        - Equal To(`==`)
        - Equal value and Equal type(`===`)
        - Not Equal(`!=`)
        - Not Equal value or Not Equal type(`!==`)
        - Greater than(`>`)
        - Less than(`<`)
        - Greater than or Equal to(`>=`)
        - Less than or Equal to(`<=`)
- Logical
    - Used to examine the logic between two variables or values
        - And (`&&`)
        - Or (`||`)
        - Not (`!`)
- Type
    - Used to determine data about a variable
        - Type of Variable (`typeof`)