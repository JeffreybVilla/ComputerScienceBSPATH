# Sorting Algorithms

### Be Familiar with bubbleSort, insertionSort, and selectionSort, how they work, and their time complexities.

## Insertion Sort Algorithm
https://www.programiz.com/dsa/insertion-sort

- Insertion sort works similar to sorting cards in our hand in a card game.
- Assume that the first card is already sorted then, we select an unsorted card.
- If the unsorted card is greater than the card in hand, it is placed on the right otherwise, to the left.
- In the same way, other unsorted cards are taken and put at their right place.

- Insertion Sort places an unsorted element at its suitable place in each iteration.


## How Insertion Sort Works?
**EX: Sort this array**
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Frame-4_0.png)
1. 1st element in the array is assumed to be sorted.
   - Take the 2nd element and store it separately in *key*.
   - Compare *key* with 1st element.
   - If 1st element is greater than *key*, then *key* is placed in front of 1st element.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Insertion-sort-0_1.png)

2. Now, first 2 elements are sorted.
   - Take 3rd element and compare it with elements on left of it.
   - Place it just behind element smaller than it.
   - If there is no element smaller than it, place it at beginning of array. 
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Insertion-sort-1_1.png)

3. Place every unsorted element at its correct position.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Insertion-sort-2_2.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Insertion-sort-3_2.png)


## Insertion Sort in C++
    #include <iostream>
    using namespace std;

    // Function to print an array
    void printArray(int array[], int size) {
      for (int i = 0; i < size; i++) {
        cout << array[i] << " ";
      }
      cout << endl;
    }

    void insertionSort(int array[], int size) {
      for (int step = 1; step < size; step++) {
        int key = array[step];
        int j = step - 1;

        // Compare key with each element on the left of it until an element smaller than
        // it is found.
        // For descending order, change key<array[j] to key>array[j].
        while (key < array[j] && j >= 0) {
          array[j + 1] = array[j];
          --j;
        }
        array[j + 1] = key;
      }
    }

    // Driver code
    int main() {
      int data[] = {9, 5, 1, 4, 3};
      int size = sizeof(data) / sizeof(data[0]);
      insertionSort(data, size);
      cout << "Sorted array in ascending order:\n";
      printArray(data, size);
    }


## Complexity
### Time Complexities
**Worst Case:** O(n^2)
- If array is in ascending order, and you want to sort in descending  order. Worst Case occurs.
- Each element has to be compared with each of the other elements so for every nth element, *n-1* number of comparisons are made.
- Total # of comparisons = n*(n-1)
  - Basically n^2
**Best Case:** O(n)
- When array is already sorted, outer loop runs for *n* number of comparisons. (Linear Complexity)

**Average Case:** O(n^2)
- It occurs when elements of the array are in jumbled order( neither ascending nor descending)

### Space Complexity
- O(1) because extra variable *key* is used


## Insertion Sort Applications
- Used when:
  - Array has small # of elements
  - few elements left to be sorted
