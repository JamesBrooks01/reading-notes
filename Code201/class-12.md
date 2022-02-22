# Reading Assignment 12

## Chart.js

---

- Charts are regarded as the better option for displaying data in comparison to tables as they are easier to look at an convey the data quickly, bu they are not always easy to create.
- A great starting place is with the JavaScript plugin called `Chart.js` that uses HTML5's canvas element to draw the graph onto the page.
  - To use it you simply download it and place the correct file into the directory and link it like any other JavaScript file.
- To start any of the charts, first you need to create a `canvas` element in the HTML ideally with an id and dimensions.
  - For a line chart you provide it with the data points and some color and label data and it will create the chart.
  - For a pie chart you simply need to provide it the color of each wedge and the value of each, obviously adding up to 100.
  - For a bar chart you provide it much the same data as line data with the colors often being RGBA for the added transparency capability.

## Canvas API

- At first glance, the `canvas` element looks like the `img` just without the `src` or `alt` elements. They `canvas` element actually only has the `width` and `height` attribute and can also can be set with DOM properties. At default it is 300px wide by 150px high. It is often used with the `id` property as well. It can also have the standard stylings of any normal image, but it doesn't affect the canvas drawing. When no styling rules are alllied, it defaults to being transparent.
- Another similarity with `img`s and similar tags is that it has fallback content for browsers that don't support the element. To provide the fallback content, you add the content between the tags and because of this, the canvas tag requires a closing tag.
- The canvas element creates a fixed size drawing that exposes one or more rendering contexts which are used to create and manipulate the content shown.
  - The canvas is initially blank and must be allowed access to the rendering context and draw on it. It gets this context with the `getContext()` method.
- Once the `canvas` is set up we have to draw on it. But before that we must understand the canvas grid or the coordinate space. Normally 1 grid unit is 1 pixel with the origin being the top left corner at (0,0). All the elements within are relative to this origin.
- Unlike `SVG` `canvas` only supports two primitive shapes, rectangles and paths which are a list of point connected lines. All other shapes are created by combining paths.
- A feature of the `Path2D` API is the ability to use `SVG` paths to make paths in the canvas. This allows you to pass around path data and re-use it in both SVG and canvas.
- To fill in color there are two main options. `fillStyle` and `strokeStyle`.
  - Both can be provided any of the CSS color values to determine the color.
  - You can also set transparency values for it.
- For styling lines the availabe properties are;
  - lineWidth
  - lineCap
  - lineJoin
  - miterLimit
  - getLineDash()
  - setLineDash()
  -lineDashOffset
- Also, just like any normal drawing program, you can fill and stroke shapes with linear, radial, and conic gradients with `CanvasGradient`.
- You can also create patterns with the `createPattern()` method with the parameters of the image and the type of pattern.
- You can also apply shadows.
- To apply text to the canvas you use the `fillText()` method or `strokeText()` methods.
  - The text can be styled with the `font`, `textAlign`, `textBaseline` and `direction` properties like with regular text.
  - If more details about the text are needed, you can also use the `measureText()` method to get the width of the text when written in the current style.