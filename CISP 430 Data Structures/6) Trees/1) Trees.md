# Tree Data Structure

- A tree is a non-linear hierarchical data structure that consists of nodes connected by edges. 

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/tree_0.png)


## Why Tree Data Structure?
- Other data structures like arrays, linked list, stack, queue are all **linear data structures** that store data sequentially.
- To perform any operation in a  linear data structure, the time complexity increases with the increase in data size.
- Different tree data structures allow quiccker and easier access to the data as it is a **NON-Linear data structure**



## Tree Terms
### Node
- A node is an entity that contains a key or value and pointers to its child nodes.
- The last nodes of each path are called **leaf** nodes that do NOT contain a link/pointer to child nodes.
- The node having at least a child node is called an **internal node**.



### Edge
- It is the link b/w any 2 nodes.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/nodes-edges_0.png)



### Root
- Topmost node of a tree.


### Height of a Node
- Height is the # of edges from the node to the deepest leaf (longest path from the node to a leaf node)

### Depth of a Node
- The # of edges from the root to the node.


### Height of a Tree
- The height of the root node or the depth of the deepest node. 
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/height-depth_0.png)


### Degree of a Node
- Total # of branches of that node. 


### Forest
- Collection of disjoint trees.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/forest_0.png)


## Types of Trees
1. Binary Tree
2. Binary Search Tree
3. AVL Tree
4. B-Tree


## Tree Applications
- Binary Search Trees are used to quickly check whether an element is present in a set or not.
- Heap is a kind of tree that is used for heap sort.
- A modified version of a tree called *Tries* is used in modern routers to store routing info.
- Most popular databases use B-Trees & T-Trees.
- Compilers use a syntax tree to validate the syntax of every program you write. 
