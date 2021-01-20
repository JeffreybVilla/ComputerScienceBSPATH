# Sorting Algorithms

### Be Familiar with bubbleSort, insertionSort, and selectionSort, how they work, and their time complexities.

## Selection Sort Algorithm

https://www.programiz.com/dsa/selection-sort

- Selection sort is an algorithm that selects the smallest element from an unsorted list in each iteration and places that element at the beginning of the unsorted list.


## How Selection Sort Works?
1. Set 1st element as *minimum*
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Selection-sort-0-initial-array.png)

2. Compare *minimum* with the 2nd element
   - If 2nd element is smaller than *minimum*, assign the 2nd element as *minimum*.
   - Compare *minimum* with the 3rd element, if the 3rd element is smaller, assign *minimum* to the 3rd element, otherwise do nothing.
   - Process continues until last element.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Selection-sort-0-comparision.png)

3. After each iteration, *minimum* is placed in the frontof the unsorted list.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Selection-sort-0-swapping.png)

4. For each iteration, indexing starts from the 1st unsorted element. Step 1 to 3 are repeated until all elements are placed at their correct positions.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Selection-sort-0.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Selection-sort-1.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Selection-sort-2.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Selection-sort-3_1.png)


## Selection Sort in C++
      // Selection sort in C++

          #include <iostream>
          using namespace std;

          // function to swap the the position of two elements
          void swap(int *a, int *b) {
            int temp = *a;
            *a = *b;
            *b = temp;
          }

          // function to print an array
          void printArray(int array[], int size) {
            for (int i = 0; i < size; i++) {
              cout << array[i] << " ";
            }
            cout << endl;
          }

          void selectionSort(int array[], int size) {
            for (int step = 0; step < size - 1; step++) {
              int min_idx = step;
              for (int i = step + 1; i < size; i++) {

                // To sort in descending order, change > to < in this line.
                // Select the minimum element in each loop.
                if (array[i] < array[min_idx])
                  min_idx = i;
              }

              // put min at the correct position
              swap(&array[min_idx], &array[step]);
            }
          }

          // driver code
          int main() {
            int data[] = {20, 12, 10, 15, 2};
            int size = sizeof(data) / sizeof(data[0]);
            selectionSort(data, size);
            cout << "Sorted array in Acsending Order:\n";
            printArray(data, size);
          }



## Complexity
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
- **Best case:** O(n^2)
  - If the array is already sorted, then there is no need for sorting.
- **Average case:** O(n^2)
  - It occurs when elements of the array are in jumbled order( neither ascending nor descending)
  
- Time complexity of selection sort is the same in all cases.
- At every step, you have to find the *minimum* element and put it in the right place.
- The *minimum* element is not known until the end of the array is reached. 


### Space Complexities
- O(1) because an extra variable *temp* is used.


## Selection Sort Applications
- Used when:
  - small list is to be sorted
  - cost of swapping doesn't matter
  - checking of all the elements is compulsory
  - cost of writing to memory matters, like in flash memory (# of writes/swaps is O(n) as compared to O(n^2) of bubble sort)
