# Reading Assignment

## Implementation: Linked Lists

---

### Big O: Analysis of Algorithm Efficiency

---

- Big O is used to define the efficiency of an alorithm or function and is evealuated on both;
  - Running Time, the time it takes to complete
  - Memory Space, the memory it takes to store the data and instructions.
- It is designed to describe the worst-case state of efficiency it can have while working. So, when evaluating an algorithm or function there are 4 key areas to examine;
  - Input Size
  - Units of Measurement
  - Orders of Growth
  - Best, Worst, and Average Case
- The input size is the size of the input parameters, it refers to both the number of parameters and the size of those parameters.
  - The higher the number, the more likely the increase in Space and Time
- The units of measurement for a function are defined as such;
  - There are three measures of time;
    - Milliseconds from start to finish(Rarely used due to the variety of power in user machines, but still a measue of run-time)
    - Number of operations executed(Number of lines of code from start to finish)
    - Number of "Basic Operations" executed(The operation contrbuting the most run-time)
  - There are four measures of space;
    - Amount of space to hold the Algorithm(Number of bytes for the characters that make up the code)
    - Amount of space to hold the input data
    - Amount of space for the output data
    - Amount of space for the "Working Space"(The creations of variables and reference points as the function calls.)
- It is of note that modern computers have enough memory that Memory Space is less of a concern now than it used to be.
- To describe the overall efficiency we use the input size `n` and measure the Space and Time required for the input size with the Order of Growth representing the increase.
- The most common notations are;
  - O(1) for code that runs in the same amount of Space or Time regardless of the input size.
  - O(log n) for code that grows logarithmicly where the rate of increase slows down as the input size increases
  - O(n) for code that grows in Space or Time in proportion to the input size.

### Linked Lists

---

- A linked list is a sequence of nodes that are linked together with the defining feature being that each node is linked to the next.
- There are two types, Singly and Doubly
- Some helpful terminology is;
  - Linked List - A linked set of nodes with each node pointing to the next one in the sequence
  - Singly - There is only one reference, The next node
  - Doubly - There are two references, The next node and the previous node
  - Node - The individual items inside a linked list, each node contains the data for that link
  - Next - The property that contains the reference to the next node
  - Head - The reference to the first node in the linked list
  - Current - The node currently being looked at
- When traversing through a linked list, you cannot use a `foreach` or `for` loop because it cannot use the important `Next` value to get to the next node.
- The best way to approach the issue is with a `while` loop to check that the `Next` node is not `null`. If you try to traverse to a `null` node an exception is raised.
- When traversing, the `Current` variable will tell where in the linked list you are.
- If you want to find if a value is in a linked list, using a basic function to search the list will have the Big O be O(n) for time and O(1) for space.
- To make adding a node to a linked list O(1), you have to replace the current `Head` without losing any references.
- To add to the middle is a bit different and will end up being O(n) for time, and O(1) for space.
- To print out all the elements of a linked list is similar to what is done in checking if an element is included, by using a `while` loop and the `Current` node to traverse.

### What’s a Linked List, Anyway

---

- A linked List is a linear data structure, meaning that there is sequence and order to their construction and the traversal.
- They operate on the opposite side to non-linear data structures where the items don't have to be in order and can be traversed non-sequencially
- The biggest difference between Linked Lists and Arrays are how the manage the memory they use.
  - Arrays require continuous memory allocation
  - Linked lists are dynamic and only need the pure space, the bytes can be scattered and still work.
- Another fundamental difference between them is that;
  - Arrays are static and Linked Lists are dynamic;
  - A static data structure needs all it's resources allocated from the start and thus if the block it's in runs out of consecutive bytes, it has to be copied and recreated with more space.
  - A dynamic data structure and grow and shrink freely because it can be scattered throughout the memory happily.
- Now, the question then is how a Linked List can have it's data scattered.
  - The answer to that is `Node`s.
- A linked list can be small or big, but will still have the same simple parts.
- Each linked list is made of node which are the elements fo the list with the first node in the sequence called the `Head` and without this `Head` node the code wouldn't know where to start.
- The end of the list simply links to `null` or an empty value.
- Each node has two parts, the data it holds and the reference to the next node in the sequence.
- Any single node has no information about how long the list is, or even where it starts, it only cares about what data it holds and what the next node is.
- This simplicity is why it can be dynamic.
- There are also multiple types of linked lists.
  - Singly linked lists only have one path that can be taken, from the Head, down the links until you reach the end of null
  - Doubly linked lists have an additional reference to the previous node and this allows the list to be read and traversed backwards as well as forwards.
  - Circular linked lists have a node that acts as the `tail` of the list and this acts as the beginning node that links to the rest of the list with the first and last element pointing to each other, making a metaphorical circle.
    - This makes adding nodes to the end easy

---

- Big O is better described as a representation of the rate of growth in an algorithm than as a real representation of run-time or run-space.
- In reference to linked lists, they are often O(1) or O(n).
  - Adding a node to the beginning is O(1) and adding to the end or middle are O(n).
- Now, to decide when is the time to use a linked list and when not to.
  - A good way to decide is that a linked list is usually efficient when adding and removing most elements but is slow to search and find a single element.
  - If something requires a lot of traversal, iteration or quick access then probably it's best not to use a linked list.
  - However, it you just need to add a bunch of data to a convientient list and don't need to worry too much about retrieving them later, a linked list could be just right.
