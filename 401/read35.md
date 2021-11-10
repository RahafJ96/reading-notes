# Graph: Graphs
A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

## Here is some common terminology used when working with Graphs:

1. **Vertex**-  also called a "node", is a data object that can have zero or more adjacent vertices.
2. **Edge**- An edge is a connection between two nodes.
3. **Neighbor** - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4. **Degree** - The degree of a vertex is the number of edges connected to that vertex.

---
## Undirected Graphs

- An Undirected Graph is a graph where each edge is undirected or bi-directional. 
- The undirected graph does not move in any direction.
- No directions to point to specific vertices but the connection is bidirectional.


## Directed Graphs (Digraph)
- A Directed Graph also called a Digraph is a graph where every edge is directed.



## Complete vs Connected vs Disconnected
- ***The three different types are completed, connected, and disconnected.***

### - Complete Graphs
A complete graph is when all nodes are connected to all other nodes.

### - Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.


### - Disconnected
A disconnected graph is a graph where some vertices may not have edges.

## Acyclic vs Cyclic

### 1. Acyclic Graph
An acyclic graph is a directed graph without cycles.

![AcyclicGraph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/threeAcyclic.png)  

- A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.

### 2. Cyclic Graph
A Cyclic graph is a graph that has cycles.

![CyclicGraph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/cyclic.PNG)  

## Graph Representation
- **We represent graphs through:**

### 1. Adjacency Matrix
- An Adjacency matrix is represented through a 2-dimensional array. 
- If there are n vertices, then we are looking at an n x n Boolean matrix

### 2. Adjacency List

- An adjacency list is the most common way to represent graphs.
- An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.
- Adjacency lists make it easy to view if one vertices connects to another.



## Weighted Graphs
- A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights. This is what a weighted graph looks like:

![WeightedGraphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightGraph.PNG)  

- When representing a weighted graph in a matrix, you set the element in the 2D array to represent the actual weight between the two paths. 

![WeightedGraphMatrix](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightMatrix.PNG) 

Within adjacency lists, you must include both the weight and the name of the adjacent vertex.

![WeightedGraphAdjacency](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightList.PNG) 


- A great way to represent the {vertices, weight} connection is through some sort of key/value pair data structure.


## Traversals


### Breadth First
- In a breadth first traversal, you are starting at a specific vertex/node. 
- This node must be specified when calling the BreadthFirst() method. 
- The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. 
- Traversing a graph that has cycles will result in an infinite loop….this is bad. 
- To prevent such behavior. Upon each visit, we’ll add the previously-unvisited vertex to a visited set, so we know not to visit it again as traversal continues.


- **Here is what the algorithm breadth first traversal looks like:**

1. `Enqueue` the declared start node into the Queue.
2. Create a loop that will run while the node still has nodes present.
3. `Dequeue` the first node from the queue
4. if the `Dequeue‘d` node has unvisited child nodes, add the unvisited children to `visited` set and insert them into the queue.

![TRacel](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/BreadthFirst.PNG)

### Depth First
In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree. 
Similar to how the breadth-first uses a queue, we are going to use a Stack for our depth-first traversal.

The algorithm for a depth first traversal is as follows:

1. **Push** the root node into the stack
2. Start a while loop while the stack is not empty
3. **Peek** at the top node in the stack
4. If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
5. If the top node does not have any unvisited children, Pop that node off the stack
6. repeat until the stack is empty.

## Real World Uses of Graphs

- GPS and Mapping
- Driving Directions
- Social Networks
- Airline Traffic
- Netflix uses graphs for suggestions of products











