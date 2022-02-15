# Reading Assignment 06

## Articles

---

### Understanding the Problem Domain

- A problem domain is in essence, what a program is designed to do. What problem it solves.
- The hardest part of understanding the problem domain is that in the real world it is often like a jigsaw puzzle with no picture. Without the big picture of the problem domain, it is harder to break the code down into understandable and workable chunks that make the code easier to do.
  - The author of the article details a case in which he had a perfectly defined problem domain when he worked at Hewlett Packard(HP), where he was writing the software for some of their printers. He was given the specs of the printer and what they wanted the printer to do in all the possible use cases and he was able to write out the code they needed with extreme ease.
- He further states that the more he codes, the more he learns and believes that fully understanding the problem he needs to solve is the most important part of the process. If you don't know the question to be answered, you cannot give a clear answer.
- So the question then becomes, What can we do to make this less of a problem? The author says that we have two options;
  - Make the Problem Domain easier
    - Developers can often make a problem domain easier by reducing the use cases and focusing on a particular part of the problem needing to be solved.
    - An example of this concept is in Video Games where you start off with a simple start of the game with guided instructions and minimal set of things you can do, then as the game progresses you get more things to do and more tools to do them with, slowly building a comprehensive understanding of the problem domain the game has.
  - Get better at understanding the problem domain.
    - As developers it is easy to fall into the trap of thinking that you understand enough of the problem to start coding without having a detailed conversation with the person who has the most understanding of the problem domain, often the person hiring you to write the code. It is therefore best to spend some time talking with the person and making sure you understand the problem domain before writing out your code. It is much more time consuming and sometimes even expensive to do things over again than it is to do it correctly the first time.

### The Difference between Primitive Values and Object References

- All data types in JavaScript are either `primitive values` or `object references`. Both of these behave differently with the main differences being in how variables are assigned, how equality operators get their output and how the programs run in general. The understanding of the differences is crucial to mastering JavaScript.
- What JavaScript types are each category
  - JavaScript has 8 different data types with 7 primitive values and `Objects`. The full list is;
    - `Boolean`
    - `Null`
    - `Undefined`
    - `Number`
    - `BigInt`
    - `String`
    - `Symbol`
    - `Object`
  - If a coder is new to JavaScript the list may look wierd or incomplete. `Arrays`, `Functions`, and `Dates` are all missing. That is because they are actually `Objects`.
- The difference between a value and a reference
  - Both `Primitive Values` and `Object References` are stored in different ways.
    - When a `PV` is assigned to a variable, the variable is set to that value directly.
    - When a variable is assigned an `object`, it differs. Instead of containing the value, it contains a reference to it.
    - When code is executed with a variable assigned an `object`, it creates the object and stores it somewhere in memory and the variable contains a reference to the memory address of the `object`.
    - In much the same way a street address doesn't contain all the information about a house, merely where it is located.
- The difference between a immutable and mutable data
  - One key difference between `PV`'s and `OR`'s is the mutability of the data. A `PV` is immutable, meaning that once the variable is created, it can be read, but you cannot write over parts of the data. It can only be replaced with a new set of data. for example; `let testWord = 'word'` then `testWord = 'test'` would work but `testWord[0] = 'Z'` would not.
  - On the other hand `Arrays` are mutable, they can be altered directly. There is no need to assign a new value since you can edit the existing array directly.
  - As for how they affect variable assignment, because `OR` only create a reference the data in the memory, problems can be run into when changing the values of `objects` is that unless done carefully, reassigning the value of an `object` that has another `object` both referencing the same data address, it can change the data for both of them potentially causing issues.
- How `PV`'s and `OR`'s affect Equality Comparisons.
  - JavaScript often uses `equality operators` to check if two `values` are the same using either `Loose Equality` with `==` or `Strict Equality` with `===`.
    - `Loose Equality` will return `true` if the values are the same.
    - `Strict Equality` will return `true` if the value and the type of value are the same.
    - Because of this difference it is recommended to use `Strict Equality` whenever possible to avoid unexpected behavior.
  - Since `PV`'s assign values, the `equality operations` result in what is to be expected, but `OR`'s are different.
  - With `OR`'s however, because they don't contain the value directly, only a reference, it can cause results that can confuse new coders.
    - If a new object is created every time, then even if the values and types might seem the same, they aren't because they are referencing different data addresses. If a duplicate reference is created, the equality check would return true. To check if the contents of two objects are the same, not the references you can either `iterate` through the `object` and check if each `key` and `value` match or convert the object to a suitable primitive before comparison.
- In summation;
  - JavaScript has 8 data types, 7 of which are `primitive values` and many common data types like `arrays`, `functions` and `dates`, are `object references`.
  - `Primitive Values` store data directly, `Object References` store a reference to the data location in memory.
  - `PV`'s are Immutable and cannot be changed after creation, `OR`'s are mutable and can be changed.
  - Since `OR`'s are stored as references, special care must be taken when duplicating objects and making equality checks.
  - While how these operations work is hard, once you understand them you can make greater and faster progress past the beginning stages in JavaScript programming.

## JS

---

### Object Literals

- Objects group together variables and functions and within these objects, they take on new names.
  - Variables become properties
    - Properties provide information about whatever the object needs, in an example of a hotel, it would say how many rooms it has or it's name.
  - Functions become methods.
    - Methods are tasks associated with the object. Again with a hotel example, it would calculate how many available rooms there are.
- Like variables and named functions, Objects have names and values. In objects, the name is called the `key`. And like variables and functions, there cannot be two identical keys in an object.
- The value of a property can be of any data type, and the value of a method is always a function.
- There are several ways to create objects, of which the easiest and most popular way is with `Literal Notation`.
  - The object is composed of a set of curly braces and their contents. The object reference is stored in a variable of whatever name it is given.
  - Each key is separated from it's value with a colon and each property and method is seperated with a comma.
- When accessing an object, you can either use `dot notation` or `bracket notation`.
  - `Dot Notation` is the name of the object followed by a period and then the name of the property or method you are accessing. `object.property`.
  - `Bracket Notation` is the name of the object followed by the name of the property or method within quotations enclosed within square brackets. `object('property')`.
  - Generally people will always use `Dot Notation` in every situation it cannot be used in such as, when the property has a name that is a number or a variable is being used in place of a property name.

### Document Object Model

- The Document Object Model or `DOM` is how browsers create models of `HTML` pages and how JavaScript can access and update the contents of a webpage.
- The `DOM Tree` is an object model that tells a browser how to structure the contents with every part of the page loaded within the browser window being represented by a manipulatable `object`.
- Methods that find elements in the `DOM tree` are called `DOM Queries`. If you need to access an element more than once it should be stored as a variable.
- when a script selects an element to access or update it first has to find it in the `DOM Tree`. For example, `getElementById('infoButton');` would search the `DOM Tree` for the element with an `id` of `infoButton`. Once it has found what it is looking for, it can work with it, any child element it has, and it's parent element(if any).
- Like with `Object References`, storing an element in a variable is actually storing the location of the element in the `DOM Tree`.
- The two main methods of searching the `DOM Tree` are `getElementById()` and `querySelector()`. Both of which can search an entire document and return individual elements, but there are key differences between them.
  - `getElementById` is the quickest and most efficient because no two elements can share the same `id`.
  - `querySelector` is a more recent addition but is very flexible because it's parameter is a `CSS Selector` which means it can target more elements.
- When a `DOM` method can return more than one element, it returns them as a `NodeList` even if it only finds one matching element.
- While `NodeLists` have similarities with `arrays`, they are not actually `arrays`, but another type of `object` called a `collection`.
- To select a specific element from a `NodeList` you can either use the `item()` method or array syntax.
  - The `item()` method where you specify the index number of the element you want as the parameter for the method.
  - Array Syntax is preferred over `item()` because it is faster to execute. To use Array Syntax, you specify the index number in square brackets.
- When you have a NodeList, you can loop through each node to apply the same statements to each.
- There are two different methods to add and remove content from a `DOM Tree`, `innerHTML` and `DOM Manipulation`.
  - The `innerHTML` property can be used on any element node and it can be used to retrieve and replace content. To update an element, you add it as a string.
    - However, there are potential security risks with doing it this way.
  - Using `DOM Manipulation` targets individual nodes in the `DOM Tree` whereas `innerHTML` is better used for updating entire fragments.
  - `DOM Manipulation` is safer to use, but is slower and requires more code.
    - `DOM Manipulation` refers to the methods that allow you to create elements and text nodes then attach or remove them to the `DOM Tree`.
- Once you have the element node selected, you use properties and methods on it to change its attributes.
- `DOM Trees` have 4 types of nodes, `document`,`element`,`attribute`, and `text`.
- An element can contain multiple text nodes and other child elements that are siblings of each other.
