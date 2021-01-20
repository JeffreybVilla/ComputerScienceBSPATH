# Sorting Algorithms

### Be Familiar with bubbleSort, insertionSort, and selectionSort, how they work, and their time complexities.

## Bubble Sort
    https://www.programiz.com/dsa/bubble-sort
    https://www.studytonight.com/data-structures/bubble-sort#

- Bubble sort is an algorithm that compares the adjacent elements and swaps their positions if they're not in the intended order.
  - Order can be ascending or descending.
  
## How Bubble Sort Works?
1. Start from index = 0, compare 1st and 2nd elements.
   - If 1st element is greater than 2nd elment, they swap. 
   - Now compare 2nd and 3rd elements. Swap them if they're not in order.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Bubble-sort-0.png)

2. Same process goes on for remaining iterations/passes.
   - After each pass, the largest element from the unsorted elements is put at the end.
   - In each pass, the comparison occurs up to last unsorted element.
   - Array is sorted when all unsorted elements are placed at their correct positons.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Bubble-sort-1.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Bubble-sort-2.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Bubble-sort-3.png)

## Bubble Sort C++
    #include <iostream>
    using namespace std;

    void bubbleSort(int array[], int size) {

      // run loops two times: one for walking throught the array
      // and the other for comparison
      for (int step = 0; step < size - 1; ++step) {
        for (int i = 0; i < size - step - 1; ++i) {

          // To sort in descending order, change > to < in this line.
          if (array[i] > array[i + 1]) {

            // swap if greater is at the rear position
            int temp = array[i];
            array[i] = array[i + 1];
            array[i + 1] = temp;
          }
        }
      }
    }

    // function to print the array
    void printArray(int array[], int size) {
      for (int i = 0; i < size; ++i) {
        cout << "  " << array[i];
      }
      cout << "\n";
    }

    // driver code
    int main() {
      int data[] = {-2, 45, 0, 11, -9};
      int size = sizeof(data) / sizeof(data[0]);
      bubbleSort(data, size);
      cout << "Sorted Array in Ascending Order:\n";
      printArray(data, size);
    }

## Optimized Bubble Sort
- In regular bubble sort, ALL possible comparisons are made even if the array is already sorted.
  - Thus, execution time is increased..
- Code can be optimized by introducing extra flag variable *swapped*.
  - After each iteration, if there is no swapping taking place then, no need for performing extra loops.
  - In that case, *swapped* is set to false to prevent further iterations.
  
### Optimized Bubble Sort in C++
        #include <iostream>
        using namespace std;

        void bubbleSort(int array[], int size) {
          for (int step = 0; step < size - 1; ++step) {
            // Run loops two times: one for walking throught the array
            // and the other for comparison
            int swapped = 0;
            for (int i = 0; i < size - step - 1; ++i) {
              // To sort in descending order, change > to < in this line.
              if (array[i] > array[i + 1]) {

                // Swap if greater is at the rear position
                int temp = array[i];
                array[i] = array[i + 1];
                array[i + 1] = temp;
                swapped = 1;
              }
            }

            // If there is not swapping in the last swap, then the array is already sorted.
            if (swapped == 0)
              break;
          }
        }

        // Function to print an array
        void printArray(int array[], int size) {
          for (int i = 0; i < size; ++i) {
            cout << "  " << array[i];
          }
          cout << "\n";
        }

        // Driver code
        int main() {
          int data[] = {-2, 45, 0, 11, -9};
          int size = sizeof(data) / sizeof(data[0]);
          bubbleSort(data, size);
          cout << "Sorted Array in Ascending Order:\n";
          printArray(data, size);
        }


## Complexity
- Bubble Sort is one of the simplest sorting algorithms
- 2 loops are implemented in the algorithm. 

        **Cycle     **Number of Comparisons**
        1st             (n-1)
        2nd             (n-2)
        3rd             (n-3)
        ....            ....
        last             1

- # of comparisons: (n-1) + (n-2) + (n-3) + ... + 1 = n(n-1)/2


### Complexity: O(n^2)
- Analyze complexity by observing the # of loops
  - 2 loops so the complexity is n*n = n^2

### Time Complexities
- **Worst case:** O(n^2)
  - If we want to sort in ascending order and the array is in descending order then, worst case occurs. 
- **Best case:** O(n)
  - If the array is already sorted, then there is no need for sorting.
- **Average case:** O(n^2)
  - It occurs when elements of the array are in jumbled order( neither ascending nor descending)
  
  
### Space Complexity
- **O(1)** because an extra variable *temp* is used for swapping.
- In the optimized algorithm, the variable *swapped* adds to the space compleixty thus making it **O(2)**.

## Bubble Sort Applications
- Used when comlexity of code does not matter
- a short code is preferred.
