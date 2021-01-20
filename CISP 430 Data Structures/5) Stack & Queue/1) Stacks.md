# Stack Data Structure? (LIFO)

- Stack is an abstract type with a pre-defined capacity.
- Simple data structure that allows adding & removing elements in a certain order.
- Every time an element is added, it goes on the **top** of the stack.
  - The only element that can be removed is at the top of the stack.

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/stack-data-structure.png)


## Stack Features
1. Stack is an **ordered list** of **similar data type**
2. Stack is a **LIFO** (Last In First Out) structure.
3. *push()* function is used to insert new elements into the stack
4. *pop()* function is used to remeove an element from the stack.
   - Both insertion and removal are allowed at one end of the Stack called **Top**
5. Stack is in **Overflow** state when it is completely full.
6. Stack is in **Underflow** state when it is completely empty.


## Applications of Stack
- Simple case is to reverse a word.
  - Push a word to the stack, letter by letter, and then pop the letters from the stack to output in reverse order.
- Used for parsing.
- Used for Expression Conversion
  - Infix to Postfix
  - Postfix to Prefix
  - etc...
  
  
## Implementation of Stack Data Structure
- Use an array or a Linked list.
- Arrays are quick, but limited in size.
- Linked Lists required overhead to allocate, link, unlink, deAllocate, but not limited in size.

- We will implement stack using array.
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/stack-implementation.png)


### Algorithm for PUSH operation
1. Check if stack is **FULL** or not.
2. If the stack is full, then print error of *overflow* and exit program.
3. If the stack is not full, then increment the top and add the element.

### Algorithm for POP operation
1. Check if stack is **EMPTY** or not.
2. If the stack is empty, then print error *underflow* and exit program.
3. If the stack is not empty, then print the element at the top and decrement the top.


## C++ Implementation of Stack Data Structure w/ OOP
    # include<iostream>

    using namespace std;

    class Stack
    {
        int top;
        public:
        int a[10];  //Maximum size of Stack
        Stack()
        {
            top = -1;
        }

        // declaring all the function
        void push(int x);
        int pop();
        void isEmpty();
    };

    // function to insert data into stack
    void Stack::push(int x)
    {
        if(top >= 10)
        {
            cout << "Stack Overflow \n";
        }
        else
        {
            a[++top] = x;
            cout << "Element Inserted \n";
        }
    }

    // function to remove data from the top of the stack
    int Stack::pop()
    {
        if(top < 0)
        {
            cout << "Stack Underflow \n";
            return 0;
        }
        else
        {
            int d = a[top--];
            return d;
        }
    }

    // function to check if stack is empty
    void Stack::isEmpty()
    {
        if(top < 0)
        {
            cout << "Stack is empty \n";
        }
        else
        {
            cout << "Stack is not empty \n";
        }
    }

    // main function
    int main() {

        Stack s1;
        s1.push(10);
        s1.push(100);
        /*
            preform whatever operation you want on the stack
        */
    }
    
    - Position of Top       Status of Stack
    -1                      Stack is empty
    0                       Only 1 element in Stack
    N-1                     Stack is Full
    N                       Overflow state of Stack

## Analysis of Stack Operations
- Time Complexities of operations performed on Stack
1. **Push** O(1)
2. **POP** O(1)
3. **Top** O(1)
4. **Search** O(n)

- push() & pop() are O(1) because we always MUST insert or remove data from **TOP** of stack. 
  - 1 step process
