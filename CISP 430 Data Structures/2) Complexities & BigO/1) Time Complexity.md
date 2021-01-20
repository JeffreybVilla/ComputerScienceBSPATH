https://stackabuse.com/big-o-notation-and-algorithm-analysis-with-python-examples/
https://afteracademy.com/blog/time-and-space-complexity-analysis-of-algorithm

## Big-O Complexity Chart
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/BigOComplexityChart.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/BigOCurves.png)


## Common Data Structure Operations
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/CommonDataStructureOperations.png)

## Array Sorting Algorithms
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/ArraySortingAlgorithms.png)

# Algorithm Analysis
- Multiple ways to solve a problem using a computer program.
- Several ways to sort items in an array.
- All the different algorithms have their own pros and cons.
- An algorithm can be though of a procedure or formula to solve a particular problem.
- Question to consider is, which algorithm to use to solve a specific problem when there exists multiple solutions to the problem?

- Algorithm analysis refers to the analysis of the complexity of different algorithms and finding the most efficient algorithm to solve the problem at hand.
- BigO Notation is a statistical measure, used to describe the complexity of the algorithm. 
- Any small problem will execute quickly. But what about big problems?
- We are interested in how long the exectution time grows as the data gets bigger.
- For example, if the data size doubles, does the execution time double? Or does the execution time quadruple? Or does it halve?

- Why do we care about time complexity? It is a good measure of efficiency. 
- Some algorithms take impractical amounts of time to finish processing large data sets. 
- Time complexity is increasingly important as the amount of data stored in the world continues to grow.


## Math Review
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/mathReview1.png)
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/mathReview2.png)


## Why is Algorithm Analysis Important?
- Help us determing how "good" an algorithm is.
- Understand tradeoffs between **Time** (Execution Speed) & **Space** (Memory Size)
- Suppose a manager tells 2 employees to design an algorithm in Python that calculates the Factorial of a # entered by user.

**Employee 1:**
            def fact(n):
                product = 1
                for i in range(n):
                    product = product * (i+1)
                return product

            print (fact(5))
            
- Algorithm takes an integer as an argument.
- fact function has a variable named *product* initialized to 1.
- A loop executes from 1 to N and during each iteration, value in the *product* is multiplied by the # being iterated by the loop and the result  is storoed in the *product* variable again.
- After loop executes, the *product* variable will contain the factorial.

**Employee 2:**
- Used a recursive function to calculate the factorial of a program.
        def fact2(n):
            if n == 0:
                return 1
            else:
                return n * fact2(n-1)

        print (fact2(5))
        
- Manager must decide which algorithm to use.
- He must find the complexity of the algorithm.
- One way to find out is to find the time required to execute the algorithms.
        %timeit fact(50)
        9 µs ± 405 ns per loop (mean ± std. dev. of 7 runs, 100000 loops each)
Output says the algorithm takes 9 microseconds (plus/minus 45 nanoSeconds) per loop

%timeit fact2(50)
15.7 µs ± 427 ns per loop (mean ± std. dev. of 7 runs, 100000 loops each)
- 2nd algorithm with recursion takes 15 microseconds (plus/minus 427 nanoSeconds) per loop.


- Execution time shows that 1st algorithm is fafster compared to 2nd algorithm with recursion.
- In the case of **LARGE** inputs, the performance difference can become more significant.


- Though, execution time is not a good metric to measure the complexity of an algorithm since it depends upon the hardware.
- Big O notation is a more objective complexity analysis metric for the algorithms. 


## Algorithm Analysis with BigO  Notation
- It signifies the relationship between the input to the algorithm and the steps required to execute the algorithm.

## Common Big-O functions
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/Big-OFunctions.png)


## 2 Methods to determine time complexity.
### Emperical Measurement of Execution Time
- Run the alg and measure execution time for various inputs, N.
- Graph "size of problem", N, vs "Execution Time" and compare shape of curve to common BigO curves.
- Actual execution time is proportional to # of operations performed, we can also use # of operations as proxy for actual time.
- **PROS:** Can be applied to complex code that is too difficult to analyze.
- **CONS** Some algorithms take a LOOOOOOONG time.

### Running Time Analysis and Rules of Thumb
- Analyze code visually rather than running code
- **Iteration Rules:**
  - Ignore simple constant time O(1) lines
    - initializations
    - lines that execute a few times
    - tests that are constant time
  - **Consecutive statements:** Only largest (Worst Case) is considered.
  - **If/else:** Consider time of of test plus time of largest branch.
  - **For loops:** Time for statements inside the loop times the loop size (# of iterations)
  - **Nested loops:** Time of the inside loop multiplied by the time of outer loop.
  - **Sequence of Code Blocks:** Ignore the block with the smaller time. 
  
  
### O(N)
            for (i = 1; i <= N; i++)
             sum = sum + i;
### O(N^2)
            for (int i = 0; i < N; i++)
             for (int j = 0; j < N; j++)
             x++;

### O(N^3)
            for (int i = 0; i < N; i++)
             for (int j = 0; j < N; j++)
             for(int k = 0; k < N; k++)
             x++;

### O(N^2) 2nd clode block wins, 1st block ignored
            for (i = 0; i <= N; i++)
             sum = sum + i;
            for (int j = 0; j < N; j++)
             for (int k = 0; k < N; k++)
             x++;
             
### O(N) 
            if(some_condition_is_true)
             for (i = 0; i <= N; i++)
             sum = sum + i;
            else
             x = x + 1;
- Pick worst case & assume conditional is always true because that will give us the loop's time.
