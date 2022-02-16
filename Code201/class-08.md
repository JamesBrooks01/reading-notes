# Reading Assignment 08

## Learn CSS - Layout

---

- In the earliest days of the internet, anything that had a design more complex than a simple document used a `<table>` element. When CSS was widely adopted by browsers in the late 90s however, designing websites became easier to do with more depth and complexity. CSS allowed developers to change how a site looked without touching HTML. As the need for better web design and better web technology has risen, so too has the evolution of CSS.
- CSS has many ways to organize the layout of the page, but first we need to understand the `display` property.
  - The display property does two main things, First it determines if the box it applies to is `inline` or `block`.
    - Inline elements behave like the words in a sentance, they all sit next to each other. Elements which are used to style pieces of text like `<span>` and `<strong>` are inline by default.
      - You cannot set an expicit width or height for an inlin element and any block level margin or padding is ignored by surrounding elements.
    - Block Lebel elements however, don't sit next to each other. They each take up their own line on the page and unless changed by CSS code, a block element will span the full width of the text in horizontal writing mode. THe margin on all sides will still be respected though.
  - The other thing the `display` property does is determine how any child elements of the attached element behave. For example, if the `display` property is set to `flex` it will make the box block level and all child elemets flex items.
- There are two main layout mechanism that handle rules for multiple elements, `flexbox` and `grid`. They may share some similarities, but they are designed to solve different layout problems.
  - `Flexbox` is designed for one-dimensional layouts, layouts that go across one direction, vertical or horizontal. At default, it will align elements next to each other and stretch them to make them the same height.
  - Items will stay on the same axis and won't wrap if they run out of space. Instead they will squash onto the same line. To change this behavior, you can use the `align-items`, `justify-content`, and `flex-wrap` properties.
  - `Flexbox` also converts all child elemnts to be flex items so they can be changed with CSS rules.
  - `Grid` looks similar to `flexbox` but is designed to control layouts on multiple axes. It allows you to write layout rules on any element that has the `display: grid` property and has a few new functions like `repeat()` and `minmax()`.
- If not in `Grid` or `Flexbox` then the elements display in normal flow. There are many different methods that can be used to change the behavior and position of items in normal flow.
- One example is `inline-block`, a display property that causes surrounding elements to obey block margin and padding. `inline-block` has some of the characteristics of a block level element but still flows inline with text.
- Another example is `float`. It is often used when you have an image that you want text to wrap around. The `float` property causes elements to float in a particular direction, allowing the sibling elements to wrap around it.
- If you have a long list, you can set it to have columns with the `column-count` or `column-width` properties.
- Another of the layout mechanisms is the `position` property. This property changes how an element behaves in noraml flow and how it relates to other elements. The options are;
  - `Relative`
    - Relative moves the element based on its current position and makes the child elements have the `Absolute` property
  - `Absolute`
    - Breaks the element out of the normal flow and because of this it can be moved in all 4 relative directions and the content surrounding it will reflow to fill the space left by it.
  - `Fixed`
    - `Fixed` behave similar to `Absolute` with it's parent instead being the HTML element itself. This means it moves wherever it is directed and stays there irrespective of what's in the way even as the viewport scrolls.
  - `Sticky`
    - In some cases, the `Sticky` property can fit the purposes better than `Fixed` as it remains where it is place within the viewport of the screen but when the viewport scrolls past it, the element follows it remaining within view in the same position until it reachs the bottom of it's parent element.

## Duckett CSS Layout

---

### Positioning

- `Static`
  - In static positioning or normal flow, all the elements stack top down depending on the order they are written in the HTML, since this is how most browsers handle the elements, you don't need to indicate it in the CSS.
- `Relative`
  - In relative positioning the elements selected can be moved in relation to the parent element in the 4 directions.
- `Absolute`
  - In absolute positioning the elements move outside normal flow and doesn't affect the positioning of other elements.
- `Fixed`
  - Fixed positioning is similar to `Absolute` positioning but when the viewport moves, it doesn't. It always remains where it is set. This is mostly used for headers with links to other areas of the website and other such things.
- `Z-Index`
  - When the three previous positionings are used, they can overlap with other elements and when overlap occurs, the elements that come later in the code will display on top of ones that come earlier. If you want a specific element to display over others, you ise the `z-index` property where you assign it a value and the higher that value is, the closer it is to the top in relation to other `z-index` values.
- `Float`
  - The float positioning moves an element within normal flow as far to the designated side as it can. Anything else within the containing element will flow around it if it can.

### Screen Size and Page Size

- Different users will have different devices with different size screens, so the content of the page has to be desigined in a way that it can work on a variety of screens. From screens as small as 3.5 inches, up to some being 27 inches or bigger and a variety of resolutions from as small as 960x640, to as large as 3840x2160 with 4k displays. With an increase in resolution, the smaller things can appear if they aren't designed to scale with the size of the display.
- The dominent standard for designing a website is to make it 960-1000 pixels wide since that is the average smallest resolution most people will be able to display.
  - In some of the earlier years designers also wrestled with how many pixels tall they should design for the amount of content could be seen without scrolling. The general consensus was to make it 570-600 tall as a standard that most still adhere to.
- There are two classes of layouts to be used;
  - Fixed Width doesn't change sizes as the window size changes with measurements typically given in pixels.
  - Liquid Width grows and shrinks as the window size changes.
- Both layouts have their advantages and disadvantages, mostly around fixed being easier to make things appear exactly where the designer wants at the disadvantage of either being too big or small when displayed on a different sized screen. And liquid scaling with the window for easier readability unless it gets too big and the layout creates gaps or text extends too far.
