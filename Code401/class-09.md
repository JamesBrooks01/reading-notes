# Reading Assignment 09

## Ten Thousand 4

---

### Dunder Methods

---

- Dunder methods are special methods that are pre-defined and add functionality to classes. One use it to emulate the behavior for built in types.
  - Such as `__len__` which would return whatever it is set to return when calling `len()` on a class it is a part of.
  - Or `__getitem__` which acts like a slice.
- This design is refered to as the Python Data Model. It can be imaginged as a powerful API that you interface with by using dunder methods.
- To have the class run something on initialization such as declaring variables local to each class instance you use `__init__`
- Next, to provide a string representation of the class you use the `__str__` dunder for an informal or nicly printible, or `__repr__` for the formal or unambiguous version.
- Three dunders for iteration are(assuming the object is using a list, or keepign track of numbers to return);
  - `__len__` which is discussed previously to return a number when called on the class object.
  - `__getitem__` which would depending on set up, return a specific thing within the class using slice syntax.
  - `reversed` which would depending on set up return the content of the object reversed.
- Some dunders for operations would be;
  - `__eq__` for comparing two values to be equal
  - `__lt__` for comparing two values to be less than
  - `__gt__` for greater than
- The list of dunders that can be used goes on.
- You can even have the class be able to be called like a functions with `__call__`

### Statistics - Probability

---

Probability is at it's most basic, "What are the chances of something happening?"

This something can be anything, often something of interest and to calculate the chances of this something happening, you also need to consider the other things that could happen. A basic example is that of a coin toss in which unless you want to get super specific only has two outcomes, heads or tails.

These two events are the `sample space` or the set of events that could happen. To calculate the probability of any event happening, we count how many times our event of interest can occur and divide it by the sample space, so in the example of a tossed coin, it has a 1 in 2 chance of being heads or tails.

However, this calculation is only a prediction and anyone who has spent time endllessly flipping a coin out of boredom, you are likely to get a large number of heads or tails for a stretch of time and so to avoid making an assumption on how fair this coin is, you gather data and with this data, often called statistics, you use these statistics to calculate the probabilities based on real-world observations and check how it compares to the ideal.

In an example of tossing a coin, if you were to flip the coin 10 times, this set woul be know as the trial and the data point we observe will be how many times it lands on heads. Now, this one trial will not be likely to reach the ideal probability but over many trials we could expect the average number of heads to get close.

Now, the probability of a coin landing on a particular side is merely an introductory example. Probability if given enough data, could theoretically provide the chances of someone developing a particular disease over time, or the chances of a car part breaking while driving.

Now, to takle any question in which you have a large amount of data, the answers will often fall in a range. By using the "normal distribution" a sort of bell curve looking graph, you can by looking at what statistic is in the middle of the bell curve to determine which is the most probable answer to the question or the most likely event to occur.

### Intro to Statistics

---

- Will watch the video tommorrow and resubmit

### AI Guru makes $238,800 with misleading paid course. doesn’t credit developers

---

- Will watch the video tommorrow and resubmit
