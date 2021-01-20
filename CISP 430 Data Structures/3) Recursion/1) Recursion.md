# Recursion
- a function that calls itself

### Infinite Recursion
- function calls itself repeatedly until error
- will get "stack overflow" error 

### EX: Infinite Recursion
main()
{
  f1();
}
  f1()
{
 f1();
}

### Mutual Recursion
- f1 calls f2 calls f1 calls f2

### EX: Mutual Recursion
main()
{
f1();
}
f1()
{
f2();
}
f2()
{
f1();
}

### Memory Usage

- Only 1 copy of the function's *instructions*, but, a new "instance" of the function's *data* is created in memory.
- A set of all local variables are created on the stack for each instance
  - an unctrolled recursion ccan use up whole stack
  
- Recursion done by accident will result in stack overflow error.
- Intentionally, a function **MUST** have a conditional to control if function will call itself or not.


### Recursion Ex: 1
    void f(int n) // O(N)
    {
    cout << n << endl;
    n--;
    if (n > 0)
    f(n);
    }

    int main(void)
    {
    f(5);
    }
    /*
    5
    4
    3
    2
    1
    */



### Recursion Ex: 2
    void f(int n) // O(log N)
    {
    cout << n << endl;
    if (n > 0) {
    f(n / 2);
    }
    }
    int main(void)
    {
    f(50);
    }
    /*
    Output:
    50
    25
    12
    6
    3
    1
    0
    */



## Recursion vs. Iteration
- For any problem, there is a often a recursive solution & an equivalent iterative solution.
