# Prep Assignment

## Command Line

---

### The Command Line

---

- The command line is a text-based interface for the system. Commands are entered as text and the feedback from these commands are also typically text.
- Within the terminal, the part of the operating system that defines how the terminal behaves and looks is called the Shell, there are many different ones with the most common being bash, or Bourne Again Shell.
- The terminal also has a wide variety of shortcuts to make life easier. One such example is the command history that is navigated with the arrow keys.
- Another advantage to using shortcuts is they can cut down on typos.

### Basic Navigation

---

- The most basic navigation commands are `pwd`, `ls`, and `cd`. These commands allow you to know where you are, what is contained within the location you are in, and where you want to go.
- To start, there is `pwd`, standing for Print Working Directory, and it refers to what directory the terminal is currently located in. As you navigate through your computer and work in different areas it can be easy to lose track of where you are, so this is a useful command to re-orient yourself to where you are.
- Next, it is important to know what files you have access to within the current directory. For this you use `ls` or list. Without any additional arguments it simply lists all non-hidden files and folders within the current directory.
- Now, before moving on, it is important to understand the concept of `path`. `Path`'s meaning in coding is similar to its literal meaning as it is the path you follow to get to a particular file or directory.
  - There are two types of `path`s that can be used, Absolute and Relative.
  - Within linux, the file structure is hierarchical with a single directory at the top simply called `root` and labeled with the symbol "`/`". Everything within the file system is a sub-directory of this no matter how far down in the structure you go, it is still part of the `root`.
  - An Absolute path is where a location is in relation to the `root`, they are always identified by starting with a forward slash, "`/`".
  - A Relative path is where the location is in relation to the current location.
- Paths can be built with many different code blocks with three of the important ones to know are;
  - `~` which refers to the home directory wherever it is in relation to the current location.
  - `.` refers to the current directory.
  - `..` refers to the parent directory of your current location, with enough of them you can move as far up the hierarchy as you wish.
- Now, with that in mind, to move around the system you use `cd`, meaning Change Directory. It is most often run with a single command line argument to refer to where the user wants to move to. This location is specified as a `path` and can be absolute or relative.
- Another shortcut to use as typing out these paths can be long and subject to typos is to use `Tab Completion` to allow the terminal to guess which directory or file in the location it's currently pointing to is next in the sequence.
- Tab completion can be used for almost any command and anytime you hit tab it will attempt an auto-complete. If nothing happens then there are several possible auto-completes and successive presses of tab will cycle through them until you reach the one you want.

### More About Files

---

- Before moving further ahead, it is important to full understand how files work and certain aspects of them affect them.
- For example, Everything in Linux is a file. Text file, Directories, even the Keyboard is a file. This doesn't affect what we as the user do very much but it helps with understanding certain behaviors of the system.
- Linux is an Extensionless System. This means that irrelevent of what file extension is attached to a file, Linux will figure out what kind of file something is based on its contents.
  - Because of this it can be difficult to know what type of file certain files are and thus another important command to know is `file`.
- Linux is also Case Sensitive. To Linux, `file.txt`, `File.txt`, and `filE.txt` are three different files that can be refered to and thus it matters when writing out the path to the location of it.
  - This case sensitivity also affects commands. `ls` and `lS` are two different commands that do two different things.
- Linux also cares about spaces in the names of files as on the command line a space seperates arguments and thus to deal with a space in a path you can either surround the name in quotes or use an escape character.
- Linux also has hidden files and directories. This is defined by a `.` at the start of the file name.

### Manuel Pages

---

- Use of the command line allows you a wealth of power and opportunity but it can be difficult to remember all the details of how to use certain things in it.
- Luckily there is a convenient resource that lists all the things that can be done on the command line called `Manual Pages`.
- The Manual Pages list every command available to the system, how they are run and what arguments they accept.
- To lookup the pages you use the command `man` with an option to type a specific command to lookup.
  - To exit the pages you use the `q` key.
  - You can also search by keyword with the `-k` argument for when you don't know exactly what command you need.
- A deent portion of competency and skill in using linux is knowing how to modify the behavior of the commands to best fit the needs of the situation.

### File Manipulation

---

- Now that the basics are out of the way, we can move on to the commands for manipulating the files on the system.
- The six most important ones are; `mkdir`, `rmdir`, `touch`, `cp`, `mv`, and `rm`. These commands are the equivilent of common operations that you might already be familiar with like file/folder creation and deletion as well as copying and moving.
- To make a directory you use the `mkdir`, meaning Make Directory. It is important to get into the habit of having a neat file structure to make it easier and faster to navigate and find the files you need.
  - Some of the common arguments used for this are `-p` for making parent directories where needed and `-v` for making mkdir be more clear on what it is doing when executed.
- To remove a directory you use the command `rmdir` or Remove Directory. One thing of note with the Linux Command Line method of deletion is that it doesn't have an undo button, once it is deleted, it's gone.
  - rmdir also has the -p and -v arguments and also requires the directory to be empty to delete it.
- To create a blank file, you use `touch`. However, touch is actually used to modify the access and modification times on files but when given a file name that doesn't exist in the current directory it creates it as a blank file.
- To copy a file or directory you use the `cp` command. It takes in the source path and destination path location of the copied file. When copying a file, it will name it whatever has been specified in the destination path.
- To move a file or directory you use the `mv` command. Similar to `cp` it also takes in a source and destination and will rename to what is specified on the destination path.
- To remove a file or non-empty directory you use the `rm` command. As it was with `rmdir` this removal is permanent.
- One last thing to note is that many of the linux commands including some of these have an extensive list of arguments that can be used the change the behavior of the commands and all of them are available to browse through the Manual Pages.

### Cheat Sheet

---

- When reading a Linux command, `[]` refers to an optional value and `<>` refers to a required value.
- If you wish to be non-specific with a path you can use the Wildcards `*` for zero or more characters, `?` for any single character, and `[]` to refer to a range of characters defined within the brackets.
- Within the terminal `Ctrl + C` cancels the currently running process.
