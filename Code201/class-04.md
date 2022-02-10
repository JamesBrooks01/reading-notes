# Reading Assignment 04

## HTML

---

- Links
  - Links are created with the `<a>` attribute. A user can click anything contained between the tags and the `href` attribute defines where the link leads.
  - It can be used to link to pretty much anywhere that has a link attached to it, whether that is another page on the web, or another page on the same site.
  - If only linking something that is stored locally, you can use relative links.
  - A link can also be used for linking an email address.
  - If you know the id of a specific place you wish to link to, either on your site or another's, you can have the link go directly to that location on the page.
- Layout
  - CSS interacts with HTML elements as if each one is it's own box. Each box can be `block-level` or `inline`.
    - Block Level elements take up their own line on the page
    - Inline elements flow between surrounding text.
  - Block level elements can be contained within other block level elements for example with a `<div>` element.
  - CSS has 5 main ways to position an element.
    - Normal
      - Each `block-level` element is on it's own line, pushing later content further and further down. This is the default.
    - Relative
      - This moves an element to the top, right, bottom, or left. It has no effect on surrounding elements.
    - Absolute
      - This moves an element outside of normal flow. it does not affect the positioning and moves as the user scrolls the page.
    - Fixed
      - This moves an element relative to the browser window. They don't affect the position of other elements, and do not move when the user scrolls.
    - Floating
      - This moves an element outside of normal flow, and pushes it to either the left or right and becomes an `block-level` element that other elements can flow around.

## JavaScript

---

- Functions, Methods, and Objects
  - To create a function, you first have to declare it with a name and the code it will run within curly brackets `{}`.
    - `function name() {code written here};`
  - The advantage of using a function is that it can be called any number of times to repeat the same code.
  - After declaring a function, to get it to run you have to then call it. It is called by simply typing it's name followed by a pair of parentheses `()`.
    - `exampleFunction()`
  - If the function needs outside data to run, you provide the data as parameters.
    - `exampleFunction(data1, data2) { return data1 * data2; }`
  - Some functions have data that can be returned to the code that called it. For example if the code is doing a calculation, it will return the result.
    - To get this data, you put the `return` keyword in after the code providing the relevant data.
  - To get multiple values out, you return them as an `array`.
  - The location where you declare variables matters. If you declare a variable within a function, it can only be accessed within that function.
  - A variable declared outside of a function is a global variable that can be used anywhere. However, it is subject to naming collisions with other variables that could potentially have the same name and they exist the entire time the page is loaded rather than just when the function is called. It is therefore recommended to use local variables whenever possible.

- 6 Reasons for Pair Programming
  - Pair programming is where two programmers work together on the same code at the same time. One person acts as the coder, and the other person instructing on what path the coder should take but has no direct computer input. They are thus free to think about the bigger picture, what comes next, while also scanning for errors or typos.
  - Pair programming has been researched heavily and has shown results in that it improves 6 different skills for better coding.
    - It improves efficiency by saving time later debugging and troubleshooting by having two sets of eyes paying attention to the code and how everything fits together. Also if they get stuck on something, they have double the brain power devoted to trying to solve it.
    - It is more engaging and harder to get distracted when two programmers are working together on the same code. It also helps train coders to know when to ask for help while also reducing the chance that they will need to, boosting confidence.
    - Everyone has a different approach to problem solving. If one person gets stuck, the other might have a different approach to fix a problem that they might not have considered before. It is also common that one person is more experienced in one area than the other and they can help teach the other in that area both improving the skill set of the less-knowledgeable dev, and increasing the understanding by explaining in their own words the more knowledgeable.
    - It also increases social skills by forcing good communication between devs.
    - A common step in a job interview process is a pair programming session between the applicant and a current employee which helps companies get a feel for how they will fit within the team.
    - It improves workplace readiness by being prepared for this idea early rather than having to learn it on the job.
