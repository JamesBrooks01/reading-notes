# Reading Assignment 11

## Data Analysis

---

### What is Jupyter Lab - Overview

---

- JupyterLab is a web-based user interface for Project Jupyter.
- It allows you to work with documents and other activities such as Jupyter notebooks in a flexible, integrated and extensible manner.
- With the support of Kernel-backed documents, you can write and execute code within the document you write.

### What is Jupyter Lab - Video

---

- Text, Code Consoles and Terminals
  - The text editor has syntax highlkighting and indention customizing
  - Terminals have support for OS shells.
- Common Formats
  - All the popular image formats are available for use
  - PDFs, HTML and LaTeX are also easy to read.
  - Large CSV files are also quick to load
  - JSON can be used with ease as well
- Jupyter Notebooks
  - Easy way to work with Text and Code side by side.
  - Each section is a cell that keeps the text and code contained within neat boxes.
  - Text cells are formatted with Markdown.
  - The Jupyter code cells are formatted for a certain language and should be written as such.
  - Any displayed output will be placed below the relevent cell
  - It retains variable memory

### Numpy Tutorial

---

- NumPy is a data analysis package for Python and using it can speed up the workflow and it can also interface with other Python packages.
- With NumPy, you work with multi-dimensional arrays. To start off you work with 2-dimensional arrays, otherwise called a matrix.
- In a NumPy array, the number of dimensions is called the `rank` and each dimension is the `axis`. The row is the first axis and the column is the second axis.
- You can automatically create a NumPy array with the `numpy.array` function and passing in a lst of lists will automaticaly create the array with the same rows and columns.
- With NumPy, all the elements have to be the same type.
- There are other ways to create a NumPy array, such as `np.zeros((3,4))` which would create an array 3 tall and 4 wide of all zeros.
- You can also use NumPy to read files and make the data into an array with the `numpy.genfromtxt` function.
- You can either target an element directly or use slice syntax to retrieve specific data from the array.
- NumPy also works with 1-dimensional arrays which only require a single index to retrieve data.
- You can also have more than 3 dimensions for the arrays.
- NumPy, because it is actually built off of C, the data types it stores the data as are different than python's. The important ones are;
  - `float` for numeric floating point data(3.2)
  - `int` for pure integer data
  - `string` for character data
  - `object` for Python Objects
- Data types ocaisionally end with a suffix to indicate the bits of memory such as `int32` for an integer that is 32 bit or `float64` for a float that is 64 bit.
- The `numpy.ndarray.astype` method converts the data type of an entire array to the specified data type.
  - It actually copies the entire array and returns the converted array
- You can also use NumPy to apply a mathmatical operation to an entire array, such as `array_1[:,10] + 15` which would add 15 to the specified elements and return a new array with the new info. To change the array in place would require the `+=` operator.
- This can be done with any of the mathmatical operators.
- To handle operations where the arrays aren't the same size, NumPy uses broadcasting to try and match up elements.
  - It first compares the last dimension of each array and
    - If the lengths are equal or one is length 1, then keep going
    - If the lengths aren't equal and none of the dimensions are length 1 then raise an error.
  - Continue checking the dimensions until the shorter one runs out of dimensions.
- You can also use some more complicated array methods like `numpy.ndarray.sum` which adds up all the elements in an array.
- You can also use comparison operators to see if certain rows match a value.
- One potential way to make it easier to access certain array elements is to reshape the array.
  - The simplest way is to flip the axes, so the rows become columns and columns become rows. This is done with `numpy.transpose`.
  - `numpy.ravel` turns the array 1-dimensional
  - `numpy.reshape` turns the array into a specified shape.
- To combine arrays, you can use `numpy.vstack` to stack the arrays vertically
  - Or `numpy.hstack` to stack them horizontally.
    - The arrays need the same number of rows for this to work however.
  - Or, for more general use, `numpy.concatenate` will combine arrays along the axis you specify
