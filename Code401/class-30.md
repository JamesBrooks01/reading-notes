# Reading Assignment 30

## Implementation: Hash Tables

---

### Intro to Hash Tables, What is a Hash Table, Basics of Hash Tables

- A hashtable is a data structure that uses key value pairs.
- The idea is that the hashtable stores the key and can quickly and efficiently retrieve it.
  - This is done through a hash which is the ability to encode the key that maps to a location in the data structure that can be looked at to find the value.
- Some common terminology for a hashtable are;
  - Hash, the result of an algorithm taking a string and converting it to a value.
  - Bucket, is what is contained at each index of the list of the hashtable and each index is a bucket an in the case of a collision can contain multiple key/value pairs.
  - Collisions, which are what happens when multiple keys get hashed to the same location.
- Because the key is hashed, the lookup for the location later is an O(1) operation.
- A hash code turns a key into an integer and need to be deterministic, where the output is determined only by the input.
- To hash a key, you start with the size of a list and then do some operation to it. The following is only one example;
  1. Add/multiply the ASCII values of the key together
  2. Multiply by a prime number
  3. Modulo to get the remainder when divided by the size of the list
  4. Insert at that index
- A common way to deal with potential collisions is to make each bucket a linked list.
- A hashmap often has four base internal methods;
  - `Add`, that hashs the key and inserts at the returned index number, as part of the linked list in the bucket if there is already a value there.
  - `Find`, which takes in a key and returns the correct value at that position of the hashtable for that key.
  - `Contains`, which accepts a key and returns a boolean if that key exists within the hashtable.
  - `GetHash`, which is the hashing function that determines the index positions.
