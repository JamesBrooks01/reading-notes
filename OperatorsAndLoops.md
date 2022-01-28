# Operators and Loops


## Operators

### Comparison Operators

---

A Comparison Operator compares the inputed values and returns a value based on whether the comparison is true. The inputs can be of the type Number, String, Logical, or Object. In most cases JavaScript tries to convert the two values to the same type for comparison which is often as a Number. the exception to this are the two "strict" equality operators which also check if the inputed values are the same type.<br>
The Operators are will return true if the first value is `operator` to the second value,<br>

- Equal To(`==`)
- Equal value and Equal type(`===`)
- Not Equal(`!=`)
- Not Equal value or Not Equal type(`!==`)
- Greater than(`>`)
- Less than(`<`)
- Greater than or Equal to(`>=`)
- Less than or Equal to(`<=`)

### Assignment Operators

---

An Assignment Operator assigns a value to the left input based upon the value of the right input.<br>
For Example, <br>

- '`x = y`' would assign the value of x to y
- '`x += y`' would assign the value of 'x + y' to x
- '`x -= y`' would assign the value of 'x - y' to x
- '`x *= y`' would assign the value of 'x * y' to x
- '`x /= y`' would assign the value of 'x / y' to x

And so on.

## Loops

---

Loops offer an easy way to repeat a block of code until it reachs a desired output. There are many types of loops but ultimately they all do the same thing, repeat an action a certain number of times. The difference lies in what situation is most easily resolved by a particular loop. The two most basic loops are the `for` and `while` loop.

### For Loop

---

A for loop repeats until it returns a value of `false`. When a loop executes, it takes the following steps,<br>
- The initial expression executes. 
    - This usually initiates a loop counter or declare a variable.
- The Condition is evaluated. 
    - If the value is `true`, then the loop executes. If it is `false` then the loop terminates.
- The statement executes
    - This is the content of the loop itself, i.e, "What action will repeat until desired outcome is achieved?"
- If present, the update expression is executed
    - This could be an increase of the loop counter to say that the loop has happened again, until the number of times the loop is supposed to happen is met.
- The loop returns to step 2

### While Loop

---

A While loop repeats its code while a specified condition is true.<br>
For Example,<br>
`while (x < 5) {`<br>
    `sampleCode;`<br>
    `x++;`<br>
`}`

Once the condition becomes false, the loop terminates. In this case, assuming x starts at 0 it would repeat 5 times then stop.

Make sure to have a way for the condition to become false otherwise the loop will run forever, which is bad.