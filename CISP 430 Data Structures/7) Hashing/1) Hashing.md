# Hashing
- Hashing is a technique of mapping a large set of aribtrary data to tabular indexes using a **hash function**.
- It is a method for representing dictionaries for large datasets.
- Allows lookups, updating and retrieval operation to occur in constant time O(1)

## Why Hashing is Needed?
- After storing a large amount of data, we need to perform various operations on these data.
- Linear search & binary search perform searches with time complexity O(n) & O(log(n))
- As size of dataset increases, the complexities become much higher.
- A technique that does not depend on size of data is needed.

## Hash Function
- Used for mapping each element of a dataset to indexes in the table. 



## Hash Table


## Searching

### Searching Lists
- 2 ways to search a list
  - Sequential Search
  - Binary Search
  
### Binary Search
- Used with sorted lists
- The list is bisected at each step
- Similar to searching a binary tree
- Requires O(log2(N)) time in worst case


### Sequential Search
- Used with unsorted lists
- Each element is looked at in sequence
- Requires O(N) time in worst case

## Hashing

### Direct addressing
- Can avoid searching if we simply use a large array with the  same number of addresses as key values.
  - The key value is used as an index into the data array.
- This wastes memory space if the range of addresses is large but incomplete
- Many elements are empty

### Hashing
    - Technique used to directly calculate address of an item from its key
    - Allows smaller arrays to be used rather than direct addressing
    - Hashing Algorithm allows address to be directly calculated O(1)
    - Hashing Algorithm *compresses* the range
    - Common Hashing Algorithms
      - Digit Selection: Selecting specific digts of the key
      - Division - Using the modulo of the key
   

**Example** Simple Hash Table
- Hash Algorithm: h(key) = key % 7
- The keys can be instantly retrieved by calculating hash address

      [35][ ][44][3][25][26][13]
      0   1   2   3  4   5   6

      Entries
      Key | h(key
      25    4
      3     3
      35    0
      26    5
      13    6 
      44    2


## Collisions
- Main problem with hashing
- 2 different keys produce same hashed address so collision occurs
- Avoid collisions by:
  - Chaining
  - ReHashing (Open Addressing)
  - Using a Perfect Hash function (0 Collisions)
