# Class 35

## Graphs

A graph is a non-linear data structure that can be looked at as a collection of nodes connected by line segments.

|Terms|Description|
|--|--|
|Vertex|A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.|
|Edge|An edge is a connection between two nodes.|
|Neighbor|The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.|
|Degree|The degree of a vertex is the number of edges connected to that vertex.|

### Directed vs Undirected

- `Undirected Graph` is a graph where each edge is bi-directional. This means that the undirected graph does not move in any direction.

- `Directed Graph` also called a `Digraph` is a graph where every edge is directed. Example:

![Directed Graph image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

### Complete vs Connected vs Disconnected

__Complete Graph__ - a complete graph is when all nodes are connected to all other nodes.

__Connected__ - A connected graph is a graph where all `vertices`/`nodes` have at least one edge.

__Disconnected__ - A disconnected graph is a graph where some vertices may not have edges. The stand alone nodes are also called `islands`.

### Acyclic vs Cyclic

__Acyclic Graph__ - An acyclic graph is a directed graph without cycles.

- A cycle is when a node can be traversed through and potentially end up back at itself.

- A directed acyclic graph is also called a DAG. This can be represented as what we know as a `tree`.

3 examples:
![3 examples of acyclic graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/threeAcyclic.png)

__Cyclic Graphs__ - A cyclic graph is a graph that has cycles.

- A cycle is defined as a path of postiive length that starts and ends at the same vertex.

2 examples:
![2 examples of cyclic graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/cyclic.PNG)

### Graph Representation

We represent graphs through:

1. Adjacency Matrix

1. Adjacency List

__Adjacency Matrix__ - is represented through a 2-dimensional array. If there are `n` vertices, then we are lookind at `n x n` Boolean Matrix.

- a sparse graph is when there are very few connections

- a dense graph is when there are many connections

__Adjacency List__ - is the most common way to represent graphs.

- is a colleciton of linked lists or arrays that list all of the other vertices that are connected.

- Adjacency lists make it easy to view if one vertices connects to another.

- This is what an Adjacency List looks like:
![adjacency list image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjList.PNG)
