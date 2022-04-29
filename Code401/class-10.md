# Reading Assignment 10

## Implementation: Stacks and Queues

---

### Stacks and Queues

---

- A stack is another data structure composed of Nodes. Similar to a singularly linked list, each Node references the next in stack but not the previous.
- The common terminology for a stack is;
  - `Push` for nodes or items put into the stack
  - `Pop` for nodes or items that are removed from the stack, raising an exception if empty
  - `Top` for the top of the stack
  - `Peek` for looking at the value of the `Top` Node in the stack, also raising an exception if empty
  - `IsEmpty` returns True when the stack is empty, otherwise False
- Stacks follow the concepts;
  - `FILO` for First In Last Out where the first item to enter the stack is the last to leave(pop) from the stack.
  - `LIFO` is the other side of the coint, for Last In First Out where the last item added to the stack is first to leave(pop)
- All 4 methods for interacting with a stack are O(1) as they only ever interact with the `Top` of the stack.
- As for queues the common terminology is;
  - `Enqueue` for nodes or items added to the queue
  - `Dequeue` for nodes or items removed from the queue and as before, raise an exception when empty
  - `Front` for the first node of the queue
  - `Rear` for the last node of the queue
  - `Peek` and `IsEmpty` which act the same as they do for stacks.
- Queues follow the opposite concepts as stacks with;
  - `FIFO` and `LILO` which mean First In Last Out and Last In Last Out, where it works like an ideal queue should.
- As before, all 4 methods are O(1) because they only even interact with one node regardless of length.
