# B-Trees
### Insert the following keys into a B-Tree of order 2: 10, 20, 30, 40, 50, 60, 70, 80, 90, 100
http://www.btechsmartclass.com/data_structures/b-trees.html

https://www.guru99.com/b-tree-example.html

## Definitions

**Tree:** Organizational structure for the storage and retrieval of data

**Root:** Top node of tree

**Leaf:**  Bottom nodes that don't have subtrees/children

**Keys:** Values inside of the nodes

**Binary Search Tree:** Every node has max degree of 2 (Can't have more than 2 subtrees.)
  - Left subtree: Only have nodes with values smaller than parent node.
  - Right subtree: Only have nodes with values larger than parent node.
  - Time coplexity: Search, insert, delete
    - Balanced BST: O(log(N))
    - Unbalanced BST: O(N)
    
**B-Tree (Self-Balancing)**
- Invented by Rudolf Bayer & Ed McCreight in 1972

## B-Tree Properties
- Every node has at most *m* children
- A non-leaf node with k children has k-1 keys
- The root has at least 2 children if it is not a leaf node
- Every non-leaf node (EXCEPT Root) has at least the ceiling of [m/2] children
  - EX: Order is 5, 5/2 = 2.5, Round up to 3.
- All leaves appear in the same level
- All keys/values in a node must be in **Ascending Order** of left to right.


## B-Tree Example

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/b-tree.png)


1. Left subtree: All less than 7.
2. Middle subtree Greater than 7 && Less than 16.
3. Right subtree: All greater than 16
4. Order/Degree of 5.
   - Max keys/values of 4.
   - Max 5 children/subtrees per node.
   - Root node has 3 children so it has (3-1) keys. 2 keys in root node. 
    


## B-Tree HW
- Order/Degree of 2.
  - Every node has max 2 children/subtrees
  - Every non-leaf node(!ROOT) has at least celing [m/2] children. 2/2 = 1.
  - Max keys/values of 1

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/b-treeHW.png)
