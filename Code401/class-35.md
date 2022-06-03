# Reading Assignment 35

## Implementation: Graphs

---

### Graphs

- A graph is a non-linear data structure that can be viewed as a collection of vertices connected by lines called edges.
- The common terminology for graphs are;
  - Vertex, A data object with zero or more adjacent vertices
  - Edge, A connection between vertices
  - Neighbor, The adjacent vertices that are connected by an edge
  - Degree, The number of edges connected to a vertex.
- Graphs can be Directed or Undirected.
  - A undirected graph is where each edge is bi-directional and means that the graph doesn't move in a direction.
  - A directed graph has edges that go in a direction, each nod is directed towards a specific node and a requirement for what node should be referenced next.
- Graphs can be further divided into;
  - Complete, where all the vertices are connected to all the others.
  - Connected, where all the vertices have at least one edge
  - Disconnected, where some vertices might not have edges.
- Even further, graphs can be;
  - Acyclic, which is directed without a cycle where a node can be traversed through and end up back at itself.
    - A tree is what could be referred to as a Directed Acyclic Graph(DAG)
  - Cyclic, is a graph that has cycles where a path of positive length starts and ends at the same vertex.
- Graphs are represented through;
  - Adjacency Matrices, which is represented with a two dimensional list and if there are `n` vertices it is an `n*n` matrix.
    - Each row and column is a vertex and the elements of both the column and row must add up to one if there is an edge, zero if not.
  - Adjacency Lists, a list is the more common way to show a graph and it is a collection of linked lists or lists that list all the vertices that are connected.
- There are also weighted graphs where numbers are assigned to the edges connecting vertices.
- The traversal of a graph is similar to those found for trees;
  - Breadth First, where you start at a specific vertex and traverse.
    - One thing to keep in mind is that you need to keep track of what nodes have been visited, otherwise you could get stuck if you traverse a cyclical graph.
  - Depth First, where you visit all sub-children of a certain branch and then move back up when you reach the end.
- The real world applications of graphs are numerous with the following being only a few examples;
  - GPS and mapping
  - Driving direction
  - Social networks
  - Airline traffic
  - Netflix's suggestions
