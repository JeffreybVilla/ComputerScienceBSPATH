# Graph Data Structure

- A collection of nodes that have data and are connected to other nodes.
 
EX: On facebook, everything is a node.
- User, Photo, Album, Event, Group, Page, Comment, Story, Video, Link, Note
- Anything that has data is a node.
- Every relationship  is an edge from 1 node to another.
- Whether you post a photo, join a group, like a page, etc, a new edge is created for that relationship.

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/facebook-graph.png)

- All of facebook is a collection of these nodes and edges.
- Facebook uses a graph data structure to store its data.
- A graph is a data structure (V, E)
  - A collection of vertices **V**
  - A collection of edges **E**
  - Represented as ordered pairs of vertices (u, v)
  
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/graph-vertices-edges_0.png)
  
In the graph:
V = {0, 1, 2, 3}
E = {(0,1), (0,2), (0,3), (1,2)}
G = {V, E}

## Graph Terms
- **Adjacency:** A vertex is said to be adjacent to another vertex if there is an edge connectiong them.
  - Vertices 2 & 3 are not adjacent because there is no edge b/w them.
- **Path:** A sequence of edges that allows you to go from vertex A to vertex B is called a path.
  - 0-1, 1-2, and 0-2 are paths from vertex 0 to vertex 2.
- **Directed Graph:** A graph in which an edge (u,v) doesn't mean that there is an edge (v, u) as well.
  - The edges in such a graph are represented by arrows to show the direction of the edge.


## Graph Representation
- Graphs are commonly represented in 2 ways

1. **Adjacency Matrix**
   - 2D array of V X V vertices.
   - Each row & column represent a vertex.
   
   - If the value of any element a[i][j] is 1, it represents that there is an edge connecting vertex i & vertex j.
   - Since it is an undirected graph, for edge (0,2) we need to mark edge (2,0)
     - Making the adjacency matrix symmetric about the diagonal.
   - Edge lookup (Checking if an edge exists b/w Vertex A & Vertex B) is very fast in adjacency matrix.
     - But we have to reserve space for every possible link b/w all vertices(VxV),so it requires more space.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/adjacency-matrix_1.png)

     
2. **Adjacency List**
   - Represents graph as an array of linked lists.
   - Index of the array represents a vertex and each element in its linked list represents the other vertices that form an edge with the vertex. 
   - Adjacency list is efficient in terms of storage because we only need to store the values for the edjges.
   - For a graph with millions of vertices, we can save a lot of space.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/adjacency-list.png)


## Graph Operations 
- Check if element is present in the graph.
- Graph Traversal
- Add elements(vertex, edges) to graph.
- Finding the path from 1 vertex to another.
