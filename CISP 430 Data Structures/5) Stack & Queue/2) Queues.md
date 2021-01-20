# Queue Data Structure? (FIFO)

- Queue is an abstract data type or linear data structure.
- 1st element is inserted from 1 end called the **TAIL**
- Removal of existing elements takes from the other end called **HEAD**

- **FIFO** (First In First Out)  
  - The element inserted first will be removed first.
  
- Same way how a queue system works in real life (Grocery Store Line)

- Operation to add element into queue is called **Enqueue** 
- Operation to remove element from queue is called **Dequeue**

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/introduction-to-queue.png)


## Features of Queue
1. Like stack, queue is an ordered list of elements of similar data types.
2. Queue is FIFO.
3. Once a new element is inserted into the Queue
   - All the elements inserted before the new element in the queue must be removed
   - in order to remove the new element.
4. peek() function is used to return the value of the 1st element, W/O dequeuing it. 


## Applications of Queue
- Used when we to manage any group of objects in an order in which the first 1 coming in, 
  - also gets out 1st while the others wait for their turn.
  
1. Serving requests: On a single shared resource, like a printer, CPU task, scheduling..
2. Real life: Call center phone systems use Queues to hold people calling them in an order.


## Implementation of Queue Data Structure
- Can implement using an Array, Stack, or Linked List.
- Easiest implementation is with Array.
- Initially the **head**(FRONT) & **tail**(REAR) of the queue poionts at the 1st index of the array (i = 0)
- As we add elements to queue, the **tail** keeps moving ahead
  - Always pointing to the position where the next element will be inserted
  - The **head** remains at the 1st index
  
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/implementation-of-queue.png)

- When we remove an element from Queue, there are 2 approaches.
- Approach [A]: We remove the element at the **head** position, and then 1 by 1 shift all other elements in forward position.
- Approach [B]: We remove the element from the **head** position and then move **head** to the next position.

- In approach [A] there is an **overhead of shifting the elements 1 position forward** every time we remove the 1st element.
- In approach [B] there is no such overhead, but whenever we move head 1 position ahead, after removal of 1st element, the **size on Queue is reduced by 1 space** each time.


### Algorithm for ENQUEUE
1. Check if queue is FULL or not.
2. If the queue is full, then prrint overflow error and exit program.
3. if the queue is not full, then increment the tail and add the element.


### Algorithm for DEQUEUE
1. Check if the queue is EMPTY or not.
2. If the queue is empty, then print underflow error and exit program.3
3. If the queue is not empty, then print the element at the head and increment the head.


## C++ Implementation
    /* Below program is written in C++ language */

    #include<iostream>

    using namespace std;

    #define SIZE 10

    class Queue
    {
        int a[SIZE];
        int rear;   //same as tail
        int front;  //same as head

        public:
        Queue()
        {
            rear = front = -1;
        }

        //declaring enqueue, dequeue and display functions
        void enqueue(int x);     
        int dequeue();
        void display();
    };

    // function enqueue - to add data to queue
    void Queue :: enqueue(int x)
    {
        if(front == -1) {
            front++;
        }
        if( rear == SIZE-1)
        {
            cout << "Queue is full";
        }
        else
        {
            a[++rear] = x;
        }
    }

    // function dequeue - to remove data from queue
    int Queue :: dequeue()
    {
        return a[++front];  // following approach [B], explained above
    }

    // function to display the queue elements
    void Queue :: display()
    {
        int i;
        for( i = front; i <= rear; i++)
        {
            cout << a[i] << endl;
        }
    }

    // the main function
    int main()
    {
        Queue q;
        q.enqueue(10);
        q.enqueue(100);
        q.enqueue(1000);
        q.enqueue(1001);
        q.enqueue(1002);
        q.dequeue();
        q.enqueue(1003);
        q.dequeue();
        q.dequeue();
        q.enqueue(1004);

        q.display();

        return 0;
    }

- To implement approach [A]
  - Change *dequeue* 
  - Include *for* loop which will shift all the remaining elements by 1 position. 
  
        return a[0];    //returning first element
        for (i = 0; i < tail-1; i++)    //shifting all other elements
        {
            a[i] = a[i+1];
            tail--;
        }


## Complexity Analysis of Queue Operations
- Just like stack, we know exactly on which position new elements will be added and from where an element will be removed.
- Single step operations
- **Enqueue** O(1)
- **Dequeue** O(1)
- **Size** O(1)
