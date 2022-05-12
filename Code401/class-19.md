# Reading Assignment 19

## Automation

---

### Python Regex Tutorial

- Regular Expressions, often shortened to Regex is a series of characters used to check if a pattern exists within a string.
  - Search Engines, Search and Replace tools for word processors, and other similar things use something similar to Regex.
- Regex has a number of functions that can be used such as;
  - `compile()`
  - `search()`
  - `findall()`
  - `sub()`
  - `split()`
  - and more.
- To use Regex in Python, you start of by using the code `import re` to import Regex as a module.
- The most basic usage of Regex is with an ordinary character pattern. It is often used to find a literal set of character, "Tree" would search for the string "Tree" in the string you provide it.
- Once you get into special characters is when Regex really begins to open up. They are essentially reserved meta characters that mean something specific. For example;
  - `^` means the start of the string
  - `$` means the end of the string
  - `[]` matches any single character contained within the brackets;
    - `[a,b,c]` would match a, b, or c.
    - `[a-zA-Z0-9]` would match any single character a-z, A-Z, or 0-9.
  - The most diverse character is `\` which is used to;
    - When used with a escape character following it, it will take on the special meaning of the term.
    - If the following character is not an escape character, it will be read as any other character
    - If can be used in front of meta-characters to remove their meta meaning and have them be read literally.
  - Some of the pre-defined sequences are;
    - `\w` for any letter,digit,or underscore
    - `\W` to mean anything else
    - `\s` for any whitespace character such as a space, newline, tab or return
    - `\S` for anything else
    - `\d` for any digit 0-9
    - `\D` for anything not a digit
    - You can also use repetitions to shorten up and further customize the Regex.
      - The use of `+` is to indicate repetition for the previous character or sequence one or more times from that position.
      - `*` for zero or more times from the position
      - `?` for zero or one times from that position
    - To check for a specific number of repetitions use square brackets, `{}`.
  - You can also group parts of the text with parentheses, `()`
  - Patterns cab also be greedy or non-greedy.
  - You can also add flags to further change the behavior of Regex;
    - `I` for case-insensitive matches
    - `S` for allowing `.` to match any character including newline
    - `M` to allows the start of string and end of string to also mean newlines
    - `X` for verbose to allow for comments and whitespace in the regex expression

---

### Shutil - High Level File Operations

- The `shutil` module contains high-level file operations like copying and archiving.
- `copyfile()` copies the contents of a source to the destination and raises an error if it doesn't have the permission to do so.
  - It opens regardless of type so special files cannot be copied as new special files.
- The default behavior is to read in blocks, use `-1` to read all the input at once, or a positive integer for a specific block size.
- `copy()` interprets the output name like the command line so if the named destination is a directory instead of a file, a new file is created with the base name of the source.
  - Permissions are copied too.
- `copy2()` works like copy, but includes access and modification times to the metadata
- When a file in Unix is created, permissions based on the user are created, to copy the permission from one file to another, use `copymode()`
- To copy other metadata, us `copystat()`
- Shutil also has three function for working with directory trees.
  - To copy a directory from one place to another, use `copytree()`, it will also recurse through the source tree and copy files to the destination(Which cannot exist in advance)
  - To remove a directory including it's contents, use `rmtree()`.
  - To move a file or directory, use `move()`
    - The semantics are similar to the command line
- To find a file you could use;
  - `which()` to scan a path for a named file.
- Shutil also has tools for managing archive files.
- The supported archive formats are determined by the modules and underlying libraries available.
- Use `make_archive()` to create an archive file;
  - The inputs are designed to support archiving an entire directory recursively.
  - By default it uses the current working directory.
- Shutil maintains a registry of formats that can be unpacked which can be seen with `get_unpack_formats()`
- Extract an archive with `unpack_archive()`
- You can also use Shutil to examine the local file system to see the available space.
  - The function `disk_usage()` returns a tuple of total space, the amount being used, and the amount of free space.

---

### Automation Ideas

- 4 Python Project Ideas to do with Automation
  - Automatically move files
    - It could be used to have conditional checks on a downloads folder to move files to desired folders based on the user
  - Automatically move files and rename them
    - An addition to the previous idea that also renames it, such as by date. and then use sub-folders to separate by year and month and place the files there with an appropriate name.
  - Automatically open YouTube when a favored creator uploads a video
    - This concept of monitoring a page and opening when something happens could also apply to things like monitoring a stock price for drops or raises
  - Automatically calculate compounding interest.
    - A long calculation delegated to a computer to solve is one of the most classic usages of software and this is just one small and fun example.
