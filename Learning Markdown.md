# Basic Syntax

## Heading

- You can indicate heading level based on number of how many "Number Signs" you attach, the more you add, the smaller
  - Alternativly, you can add any number of "==" or "--" symbols on the line beneath for Heading level 1 or 2
- When doing a heading, always put a space between the number sign and the heading for compatability

## Paragraphs

- For paragraphs put an empty line between lines of text
  - And unless the paragraph is a list, don't indent

## Line Breaks

- To create a line break,either use the command `<br>` or use two or more empty spaces at the end of the line
  - The use of two or more spaces is usually not reccomended as it's hard to see in a text editor

## Emphasis

- To create some emphasis you can either bold or italicize the text
  - To **bold** put two asterisks before and after a word or phrase and to *italicize* only use one asterisk
  - To ***Bold and italicize*** at the same time add three asterisks before and after.


## Blockquotes

> -  To create a Blockquote add a > in front of the paragraph
>  - A blockquote can contain multiple paragraphs you just need to add a > on the blank line between the paragraphs
>> - A blockquote can also be nested by adding another > to the line you wish to nest
> - For best compatability put a blank line before and after blockquotes


## Lists

-  You can also create ordered and unordered lists by using either numbers plus a period or dashes, for example;
1.  Item One
2.  Item 2<br>
Or,<br>
-  Item One
-  Item Two

- And if you need to put a number at the beginning of an unordered list, seperate the number and the period with a backslash
  - 1968\.

## Adding Elements to a List

- You can also add elements into lists by indenting either 4 spaces or 1 tab

### Paragraphs

1. Item One
2. Item Two

    Paragraph One
  
3. Item Three

### Blockquotes

1. Item One
2. Item Two

    > Blockquote

3. Item 3

### Code Blocks

- Code Blocks are indented 4 spaces or one tab, and when they are in a list, indent them eight spaces

### Images
  
  - To put images in, input the command `[Name](Image Location)`
    - For example,
  
  >![tux](https://user-images.githubusercontent.com/98154935/150903638-989b743e-5e65-4c64-af12-2f55d5862b9f.png)
 
### Lists
 
 - You can also nest an unordered list into an ordered list
 
  1. Item One
  2. Item Two
    - Indent Item
    - Indent Item
  3. Item Three
 
 ## Code
 
 - To label something as code, enclose it in `backticks`
  - If a word or phrase you label as code has a backtick in it you can escape it by enclosing the word or phrase in double backticks
    - ``Use 'Code' in Markdown``

## Horizontal Rule

- To create a horizontal rule use three or more asterisks, dashes or underscores on a line by themselves
  - For example,<br>
  
>---
  
- To ensure compatability, put a blank line before and after the horizontal rule

## Links

- To create a link use the format of `[Name](URL)`
  - For example, The [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet)
  - You can also add a title to the link by adding a word or phrase in quotations after the link like, `[Name](URL"Title")`
  - If you want to simply add a link or e-mail enclose it in brackets, for example<br>
    - <fake@example.com>
  - You can also emphasize links using the same method as before

### Reference Style Links

- You can also add a link that makes URLs easier to display and read by having the link be in two parts.
  - Part 1 which is inline with the text and
  - Part 2 which is stored somewhere else in the text.

#### First Part

- The first part is the inline part which you format with two sets of brackets, One set on the text that should appear to be linked, and the second should display a label that points to the link somewhere else in the document.
  - While not nescessary, you can include
