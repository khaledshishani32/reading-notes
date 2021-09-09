#  Graphs
---
### A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges

#### ome common terminology used when working with Graphs: 

- Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
- SEdge - An edge is a connection between two nodes.
- Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
- Degree - The degree of a vertex is the number of edges connected to that vertex.

---

### Directed vs Undirected :

### Undirected Graphs

#### An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

#### For example, in the graph below, Node C is connected to Node A, Node E and Node B. There are no “directions” given to point to specific vertices. The connection is bi-directional.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Undirected_graph.svg/1280px-Undirected_graph.svg.png)

---

### Directed Graphs (Digraph) .

#### A Directed Graph also called a Digraph is a graph where every edge is directed.

#### Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

#### Compare the visual below with the undirected graph above. Can you see the difference? The Digraph has arrows pointing to specific nodes.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/Directed_graph.svg/1280px-Directed_graph.svg.png)
### Weighted Graphs 

#### A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights. This is what a weighted graph looks like:
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightGraph.PNG)

#### When representing a weighted graph in a matrix, you set the element in the 2D array to represent the actual weight between the two paths. If there is not a connection between the two vertices, you can put a 0, although it is known for some people to put the infinity sign instead.

#### Using the graph from above, here is an example of what a weight matrix would look like
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightMatrix.PNG)
---

### Traversals

### Breadth First

#### In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. 

- Enqueue the declared start node into the Queue.
- Create a loop that will run while the node still has nodes present.
- Dequeue the first node from the queue
- if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/BreadthFirst.PNG)

