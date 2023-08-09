# Graph

* A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

## some common terminology used when working with Graphs:

* Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
* Edge - An edge is a connection between two nodes.
* Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
* Degree - The degree of a vertex is the number of edges connected to that vertex.

## Directed vs Undirected
1. Undirected Graphs
* An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.
* For example, in the graph below, Node C is connected to Node A, Node E and Node B. There are no “directions” given to point to specific vertices. The connection is bi-directional.

2. Directed Graphs (Digraph)
* A Directed Graph also called a Digraph is a graph where every edge is directed.
* Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.
* Compare the visual below with the undirected graph above. Can you see the difference? The Digraph has arrows pointing to specific nodes.

## Complete vs Connected vs Disconnected
* There are many different types of graphs. This depends on how connected the graphs are to other node/vertices.

* The three different types are completed, connected, and disconnected.

1. Complete Graphs
complete graph is when all nodes are connected to all other nodes.

* Take a close look at each of the vertices in the graph above. Do you notice that each vertex is actually connected to every other node on the graph? That is what makes it a complete graph.

2. Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.

* the visual above, this looks a lot more than what you are used to seeing. If you look closely at the different vertices of the graph, you will see that each node is connected to at least one other node or vertices. A Tree is a form of a connected graph. We will talk more about that in a bit.

3. Disconnected
A disconnected graph is a graph where some vertices may not have edges.

* In the above visual, the disconnected graph shows that some nodes may not always be connected to other nodes or vertices of the graph. It is complelty possible to have standalone nodes or edges (also known as islands) in a graph data structure.
  
## Acyclic vs Cyclic
* In addition to undirected and directed graphs, we also have acyclic and cyclic graphs.

1. Acyclic Graph
An acyclic graph is a directed graph without cycles.
* A cycle is when a node can be traversed through and potentially end up back at itself.
* A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.

2. Cyclic Graphs
* A Cyclic graph is a graph that has cycles.
* A cycle is defined as a path of a positive length that starts and ends at the same vertex.

## Traversals
* You will be required to traverse through a graph. The traversals itself are like those of trees. Below is a breakdown of how you would traverse a graph.

1. Breadth First
* In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. Traversing a graph that has cycles will result in an infinite loop….this is bad. To prevent such behavior, we need to have some way to keep track of whether a vertex has been “visited” before. Upon each visit, we’ll add the previously-unvisited vertex to a visited set, so we know not to visit it again as traversal continues.

* As a refresher of what breadth first actually means here it is: Breadth first traversal is when you visit all the nodes that are closest to the root as possible. From there you traverse outwards, level by level, until you have visited all the vertices/nodes.

* algorithm breadth first traversal looks like:

1. Enqueue the declared start node into the Queue.
2. Create a loop that will run while the node still has nodes present.
3. Dequeue the first node from the queue
4. if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.

2. Depth First
* In a depth first traversal, our approach is a bit different than the approach used for breadth first. While the breadth first traversal uses a Queue to visit all children at a given level, the depth first traversal uses a Stack to visit all children of a given subtree. (This differs from our approach to tree traversal, where we visit nodes via recursive calls. Recursive calls use a call stack internally.)

* The algorithm for a depth first traversal is as follows:

1. Push the root node into the Stack and mark as visited.
2. Start a while loop that runs as long as the stack is not empty.
3. Pop the top node off of the stack and check its neighbors.
4. If a neighbor hasn’t been visited, push it onto the stack and mark as visited.
5. Repeat until the stack is empty.
