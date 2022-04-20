# Reading Assignment 03

## FileIO & Exceptions

---

### Read & Write Files in Python

---

- One of the most basic and common tasks in python is reading and writing files.
- To go further into how to work with files, it is important to know what files actually are and how OSs handle some aspects of them.
- At it's most basic, a file is a set of bytes that store data. This data is organized in a specific format and can be as simple as text, or as complicated as a program executable. But, in the end all these bytes are converted into binary for the computer to use.
- On most modern OSs, files are made up of three parts;
  - The header which contains the file name, size, type, and so on.
  - The data which holds all the contents.
  - The End of File(EOF) which is a special character that defines the end of the file.
- What the data represents depends in the format used typically decided by the file extension.
- When a file is accessed the file path is required, composed of the folder path, the file name and the extension.
- A common problem encountered is the encoding of the byte data with with two most common encodings being ASCII with 128 characters and it's parent set of Unicode with 1,114,112 characters.
- To open a file in Python, you use the built-in `open()` function.
- After opening a file it is best practice to then close the file when it is no longer needed using `file_name.close()`.
- When opening a file in python, it is going to be one of three types of file;
  - Text, opened with `open('File_Name')` and the optional second argument of either `r` or `w`
  - Buffered Binary, opened with the same method, but one of two second arguments to define the opening as a reader or writer with `'rb'` or `'wb'` respectably.
  - Raw, which is opened the same way, and is opened with the `'rb'` second argument and the `buffering=0` third argument.
- Once open, you use the `.read(size=file_size_to_be_read)` method, or the `.readline()` method with the same argument. Then finally the `.readlines()` method which just reads the remaining lines and returns them.
- Some tips are;
  - The `__file__` attribute is a special attribute of modules similar to `__name__` and is the pathname of the file from which the module was loaded if loaded from a file.
  - To append to a file, you use the `file-name.write()` method.
  - To work with two files at the same time, you seperate the open methods by commas.

### Exceptions in Python

---

- In Python, the program terminates as soon as it encounters an error. These errors could be something as simple as a syntax error or something more like an exception.
- A syntax error is where the parser finds an incorrect statement, usually the error message will tell you where the error is and how to fix it.
- An exception happnes when a syntactically correct piece of code results in an error. The error message will often give you more details on exactly what kind of exception it is.
- A coder can also manually raise an exception if a specified conditon occurs.
- One way to manually raise an exception is with the `assert` code. Assert will check if a specific condition returns True or False. If it's True then the code continues on, but if it's false the code will stop and raise an AssertionError.
- One way of handling exceptions is with the `try` and `except` blocks of code.
- Python will `try` and run the code following it as a normal part of the code and any code following the `except` block will run if an exception occurs in the `try` code.
- Also, there is the `else` statement which only runs the code following it if there are no exceptions.
- Then, last in the chain is `finally`. Anything following this statement will run no matter what. A common usage of this is to have the `.close()` method be here to make sure the file closes even if an exception occurs.

### Things I want to know more about/Other Notes

- I want to finish the companion video for "Read & Write Files in Python" to see if there is any new information within it that isn't covered in the article, unfortunately all but the first two videos are locked behind the website's paid membership and thus I cannot watch them to know.
