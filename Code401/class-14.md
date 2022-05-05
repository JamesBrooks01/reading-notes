# Reading Assignment 14

## Data Visualization

---

### Matplotlib Tutorial

---

- Matplotlib is a way to visualize data from Python in many different formats.
- Matplotlib has a set of default settings that allow the cutomization of multiple properties like color, style, axis and grid properties, the text and font properties and while the defaults are good in most cases, modifying some is beneficial for specific cases.
- Most of the modifiable properties are used with the obvious name
  - color is color, adding a legend is legend then specifying the location, etc.
- A figure is the window in the user interface and within this figure can be sub-plots and while a sub-ploy positions plots on a regular grid, axes allow free placement within the figure.
- To divide a figure into subplots, you need to specify the number of rows and columns and the number of the plot.
- Axes are similar to a sub-plot but they can be placed anywhere within the figure.
- Formatting the ticks are an important part of making a publishing ready figure. Matplotlib provides an easy to use configuration system for the ticks to help.
  - There are locators to specify where they should appear, formatters to give them an appearance you want, and major and minor ticks can be locate and formatted independently.
- Matplotlib can also be used for animation. The easiest way to do this is by declaring a `FuncAnimation` object that specifies what the figure to update is, what the function is, and the delay between frames.
- The types of plots are lengthy, but important to know;
  - Regular Plot which is a line
  - Scatter Plot for a spread of data points
  - Bar Plot for each value being a rectangle sized to its value on the axis
  - Contour Plot for contour lines and filled contours
  - ImShow for displaying an image to current axes
  - Quiver Plot which is a field of arrows
  - A Pie Chart with each value being a sized pie shaped slice of the whole with the size representive of it's percentage of the whole
  - Grid
  - Multiplot for several plots at once
  - Polar Axis
  - 3D Plots
  - Text
- Each of the plot types are specified by their name as the method on `plt`