# Reading Assignmnent 09

## HTML

---

### Forms

- Forms are the most common way of gaining user imput, they are also versitile, allowing the code to gather text content, let the user make choices, and submit forms. Forms work by accepting user imput when it is submitted, processing in the programming language and returning something to the browser or user.
- Forms are structured within a `form` element and an `action` attribute to know where to send the information, and one of two methods, `get` or `post`. The code defaults to the `get` method.
- There are three main catagories for gaining user input;
  - Text
    - When setting a form to text, you can change some of the attributes to further specify and control the input box such as it's maximum length, or if it is a password or other such sensitive information.
  - Choice
    - When setting a form to choice input, you can change if it is a single selection, a checkbox, or perhaps a drop down box.
  - Submission
    - When using a submission form, you can set it to allow file input, or a simple submit button to submit the data of the forms or even have the button be an image.
- The data is sent in name/value pairs. Each form control has a name given to it and the imput are accepting.
- HTML5 introduced more form elements to make it easier for users to fill in forms.

### Lists, Tables & Forms

- Several CSS properties were designed solely to work with specific elements like, tables, lists, and forms.
  - For `Lists` you can change the style of the bullet points if it is an unordered list, or the Letter/Number if it is an ordered list or make the bullet points an image. Or you can change the position of the markers.
  - For `Tables` you can change the size of the table and the cells it contains. There are also mainline properties commonly used with tables such as the properties related to the font and padding of the content or aligning the text.
  - For `Forms`, most of the commonly used properties are for making the form look more interactive and nicer. The most common areas are the text imputs, the submit button and adding lables to forms to get everything to line up and be clear.
- These elements also work with all the other properties that work with all elements, but these are designed to work with these elements.
- Forms are easier to use if the controls are vertically aligned with CSS

## JavaScript

---

### Events

- While browsing the web, the browser can register different events as a way of telling the code that something happned which the code can then react to. The main types of events are; `UI`, `Keyboard`, `Mouse`, `Focus`, `Form`, and `Mutation`.
- To get the code to react to an event, you first provide the code with the DOM node of the element, set it to check for the event you want, and then tell it what you want it to do when/if it happens.
- In total there are three ways to bind an event to an element. `HTML Event Handelers`, Which are the old way of doing it and not recommended, `DOM Event Handlers`, which are perferred over `HEHs`, but can only bind one function to the event. And `DOM Level 2 Listeners`, which are the favored method as they can bind multiple functions to one event.
- Another thing to know is `Event Flow`. `EF` is the knowledge that when you click on an element, you are also clicking on the parent element(s) as well. This matters depending on if the flow is `Bubbling` or most specific first then out, or `Capturing` and least specific inwards for which events trigger in which order.
- Using `EF` you can also help make the code more efficient and faster by using Event Delegation to monitor the parent element for change and then target what child element actually got an event.
- The most common events are W3C DOM events but with HTML5, there are others and even browser-specific events.
