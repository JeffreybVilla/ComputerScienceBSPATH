# Linked Lists
https://www.studytonight.com/data-structures/introduction-to-linked-list#
https://www.programiz.com/dsa/linked-list

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/linked-list-1.png)

- Linear Data Structure
  - Group of nodes in a sequence
  
- Each node holds its own **data** and **address of next node** 

- Linked Lists are used to create trees and graphs


## Advantages of Linked Lists
- Dynamic, so allocates memory when required.
- Insertion & deletiion operations can be implemented easily.
- Stacks & queues can be easily executed.
- Linked Lists reduce access time.

## Disadvantages of Linked Lists
- Memory is wasted as pointers require extra memory for storage.
- No element can be accessed randomly; MUST access each node sequentially.
- Reverse traversing is difficult.

## Applications of Linked Lists
- Linked Lists used to implement stacks, queues, graphs, etc.
- LL lets you insert elements at the beginning and at the end of the list.
- With LL you don't need to know size in advanced.

## Types of Linked Lists
- 3 different implementations

1. Singly Linked List
2. Doubly Linked List
3. Circular Linked List

## Singly Linked List
- Nodes have a **data** part & an **address part**
  - *next* points to the next node in the sequence of nodes
  
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/linked-list-linear.png)


## Doubly Linked List
- Each node contains a **data** part and **2 Addresses** 
  - 1 for the **previous** node and 1 for the **next** node
  
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/linked-list-double.png)


## Circular Linked List
- The last node of the list holds the address of the first node.
  - Circular chain is formed
  
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/linked-list-circular.png)
