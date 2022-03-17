# Reading Assignment 04

## React and Forms

---

### React Docs - Forms

---

- What is a ‘Controlled Component’?
  - An imput form element which has it's value handled by React.
- Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
  - When `value` is set to the form element the displayed value will always be `this.state.value` and if `handleChange` runs on every key stroke, the displayed value will update as the user types.
- How do we target what the user is entering if we have an event handler on an input field?
  - `this.state.value`

### The Conditional (Ternary) Operator Explained

---

- Why would we use a ternary operator?
  - For simple two condition conditional checks, it can be done on one line, and even for longer checks, it is more compact and faster to write out than endless if/else statements.
- Rewrite the following statement using a ternary statement:
- `if(x===y){
  console.log(true);
} else {
  console.log(false);
}`
  - `x===y ? true : false`
