# Reading Assignment 15

## Implementation: Trees

---

### Trees

---

- When working with a new Data Structure, learning the correct terminology is helpful. For Trees, the common terminology is;
  - Node, A component which contians it's value and references to other nodes
  - Root, The node at the beginning of the tree
  - K, A number that specifies the maximum number of children nodes allowed per node. In a binary tree, K is 2
  - In a Binary Tree
    - Left, A reference to one child node
    - Right, A reference to the other child node
  - Edge, The link between a parent and child node
  - Lead, Any node that doesn't have any child nodes
  - Height, The number of edges beween the root and the furthest leaf
- As with any data structure, knowing how to traverse the tree is important. It allows us to search for a node, print the contents and more. With trees, there are two types of traversal;
  - Depth First
    - Prioritizes going through the height of the tree
    - Three methods that change the order of the prints
      - Pre-Order, Root-Left-Right
      - In-Order, Left-Root-Right
      - Post-Order, Left-Right-Root
    - The most common way to use Depth First to traverse a tree is to use recursion and rely on the call stack to navigate up the tree when reaching the end of a sub-path
  - Breadth First
    - Goes through the tree by going through each level of the tree node by node.
    - Commonly uses a queue to traverse the tree.
    - Works by enqueueing each child node node and then dequeueing the front node and then enqueueing the left and right nodes again, working through the node level by level.
- The types of trees can often be seperated into Binary Trees and K-ary Trees.
  - A k-ary tree is one that allows nodes to have more then 2 child nodes with K being representative of the maximum number of childern node is allowed to have.
  - To traverse a K-ary tree, you use an approach similar to Breadth First traversal. The difference lies in the practice of navigating down the list of child nodes rather than looking for a left and right child.
- Because trees don't have a structural rule for where nodes are supposed to go, there is not a strict rule for where nodes get placed.
  - One strategy for adding new nodes is to fill all the child spots from the top down. To find an empty spot, you traverse through the tree until you find a node that has an empty spot and then add the node there.
- The Big O for Trees is in most cases `O(n)`.
- The third type of Tree is a Binary Search Tree. In a BST nodes are organized so that values smaller than the root are placed on the left and larger are placed on the right.
  - The advantage of a BST is that they can be searched quickly as you simply have to compare the value you are searching for against the root or sub-tree and if the value is smaller, traverse the left side, if larger, traverse the right until you get to the value you want, or you run out of nodes.
  - For Big O, it is `O(h)`, where h is the height of the tree which in a balenced tree is `log(n)` and in an unbalenced one is `n`.
  - For space it is O(1) because no additional space is allocated.
  