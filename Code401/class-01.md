# Reading Assignment 01

---

## Readings: Topic

---

### Pain and Suffering

--- 

- The price of learning at an accelerated pace is pain, but we need to be careful we don't mistake pain for suffering.
- During the 10 weeks of the course we will be pushed further than before, expected to learn more at a faster pace than we will think we can handle and it will be uncomfortable. But we must remember it is pain, not suffering.
- All growth comes with some amout of pain as it pulls us out of our comfort zones and the greater and faster the growth, the more painful it will be. But, it is temporary and serves to push you forwards.
- But, to make everything clearer we must define the difference between pain and suffering.
  - Suffering is pain without purpose, without a higher goal, dream, ambition or aspiration.
  - Pain is what pushes us forwards towards a better future, while suffering only keeps us stagnent or moving backwards.

### Beginners Guide to Big O

---

- Big O Notation is how computer science describes the performance or complexity of an algorithm. It is specifically used to define the worst-case senario and describes the time or space used.
- Some examples to allow the idea to be understood better are;
  - O(1) which is an algorithm that executes in the same time or space irrelevent to it's data set.
  - O(N) which is an algorithm that grows in proportion to it's data set.
  - O(N^2) is an algorithm proportinal to the squared size of the data set.
  - O(2^N) is an algorithm that doubles with each addition to the Data Set.
- A Logarithm is tricky to explain, so a common example is a binary search that halves the size of the data set every time it performs a comparison to the target value.
  - To use numbers, 10 items takes a second, 100, takes two, and 1,000 takes three.
  - Because it halves the data set each comparison it is extremely efficient when serching large data sets.

### Names and Values in Python

---

- Names refer to values. x=23 assigns the integer of 23 to the name of x.
  - Many names can refer to one value and they are reassigned independently.
- Values live until they have no references.
- Assignment doesn't copy data.
  - If you assign and create a value then assign another name to the same value, if the original value changes, or you change the nth name of the value, it changes all of them because they all refer to the same value.
- The way around this is with immutable values or values whose value cannot change like Numbers(Int,Float), Strings, and Tuples.
- To change an Int is to rebind the name.
- To change a list is to mutate the list.
- One easy way to think of the difference is to remember that assignment is the same for all values, but Aliasing can make it seem different.
- References are more than names. List elements are references to values.
- Alot of things are actually references;
  - Object Attributes
  - List Elements
  - Dictionary Values and Keys
  - Anything on the left side of an assignment operator
- There are also alot of things that are assignments
  - x = 
  - for x in
  - class X()
  - def X()
  - import X
  - From .. import X
  - etc.
- The best way to avoid a suprise from mutable aliasing is to avoid mutating values altogether and to create a new value/list.
- Names have scope but no type, and Values have no scope but defined type.

