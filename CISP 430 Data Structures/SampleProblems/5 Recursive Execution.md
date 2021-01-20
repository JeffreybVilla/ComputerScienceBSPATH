### Draw the recursive hand execution for the following code using the graphical diagramming technique demonstrated in class and used in your homework. For each problem you must draw a box for each function instance, draw box(es) for local variables and parameters inside each function box, etc, as requested in the homework.

    main()
    {
     Pow(2, 7);
    }
    
    Pow(long int X, unsigned int N)
    {
     if (N == 0)
     return 1;
     if (N == 1)
     return X;
     if (IsEven(N))
     return Pow(X * X, N / 2);
     else
     return Pow(X * X, N / 2) * X;
    }
    
    
![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/recursiveHand.png)
