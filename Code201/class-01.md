# Reading Assignment 01

## HTML

### How People Access the Web

- To build a website, you must understand how people access the web.
  - The first layer is through their Web Browser
    - Examples include Firefox, Internet Explorer, Chrome, Opera, and others.
    - To view a webpage, they could input an address manually, follow a link, or use a previously assigned bookmark.
    - Software manufacturers are always releasing new versions so a website developer must keep in mind that not all their visitors will have the latest versions with the best functionality.
  - The second layer is the Web Server.
    - When a user asks their browser to display a webpage, it sends the request to a web server
    - Web servers are a special kind of computer that is always connected to the internet and is designed to send webpages to browsers on request.
  - The third layer is the Device the request is coming from.
    - In the modern age, people are using a wide variety of devices to access the web and website designers have to keep the fact that different devices will have a different size of screen and speed of connection than others in mind when designing them.
  - The fourth layer are Screen Readers
    - Screen readers are programs commonly used by people with vision impairments to read out the contents of a website to them.
    - In much the same way as public buildings have laws governing them that require accessibility to those with disabilities, there are laws requiring websites to be accessible to those with disabilities too.

### How Websites Are Created

- Next, You have to Understand how Websites are Created.
  - Almost always when you look at a webpage, you are seeing the data the browser receives in the format of HTML and CSS from the web server.
  - Some websites also have JavaScript or Flash within them.
  - If a website is particularly large and complex, then it may also use a database to store data and a programming language like, PHP, ASP.Net, Java or Ruby on the web server to manage it, but that is all information on the back-end and doesn't improve what the user sees.
  - Since the web's creation, there have been many versions of HTML and CSS, we are currently on HTML5 and CSS3.

### Structure

- HTML is used to describe the structure of a page through elements.
  - Each element is composed of,
    1. An opening tag,
        - Which is composed of an opening bracket, `<`, a character(s) that define what the element is, `p`, and a closing bracket, `>`.
          - `<p>`
    2. The content within the tags
        - `<p>` This is a paragraph
    3. And the closing tag
        - Which is the same as the opening except with a forward slash before the character.
          - `<p>` This is a paragraph `</p>`
- The different elements define where on a page something goes and in some cases how it looks.
  - An `<html>` element which labels everything within it as HTML code
  - A `<body>` element is composed of everything that is displayed in the main window.
  - An `<h1>` element is the main Header of the page.
  - A `<p>` element is a paragraph of text.

- Attributes further define elements and appear within the opening tag.
  - They are composed of a name and value.
    - The name defines what information is being provided
    - The value sets the information being changed.
  - For example this attribute would define that the language used is English.
    - `<p lang="en - us></p>`

### Extra Markup

- To define what version of HTML is being used, you include the DOCTYPE element at the beginning.
  - For HTML5 you put `<!DOCTYPE html>`.
- Adding comments to the code can help make code clearer for both you and anyone in the future who looks at it.
  - In HTML comments are added using `<!--` to open and `-->` to close.
- The `id` and `class` attributes are used to identify certain elements.
  - `id` is used for specific elements
  - `class` is used for a type of element
- The `<div>` and `<span>` elements are used to group elements together
- To add special characters, there are escape characters to add them.

### HTML5 Layout

- The new elements of HTML5 are used to define different parts of a page easier to both create and read.
- It also helps make the code cleaner than the old method which relied on using multiple `<div>` elements.
- To make old browsers understand HTML5, they need to be told which elements are a block-level element.

### Process & Design

- When creating a Website, it is important to know who your target audience is.
  - Questions like, Why are they on the website, what information they want and how often they are likely to return.
  - A site map is used to plan the structure of the entire site
  - A wireframe is used to plan the structure of a web page
  - Design is about communicating ideas. If a visitor doesn't understand what you are trying to tell them, they can't interact with the page properly.

## JavaScript

### How Browsers See Web Pages

- To understand how HTML content can be changed using JavaScript, you need to understand how a browser interprets the HTML code and displays it.
  - First, the browser receives the raw code.
  - Second, the browser creates a model of the page that defines what elements are part of what.
  - Third, it uses a rendering engine to display the page. If no CSS is provided, it will assign the defaults style for each element.
- If the page has Javascript, it runs the code through the browser's scripting engine, otherwise called an interpreter. The Interpreter turns the JavaScript code into a set of instructions for the browser to follow that it goes through one-by-one.

### How to use Objects and Methods

- JavaScript is built off of Objects and Methods.
  - Objects define what area of influence the JavaScript will be changing.
  - Methods define how it's changing.
- The JavaScript `console.log()` would write to the console whatever is between the parenthesis for example.
- JavaScript runs where in the HTML it is. If the browser encounters a `<script>` tag, the browser loads the script within and checks if it needs to do anything.
