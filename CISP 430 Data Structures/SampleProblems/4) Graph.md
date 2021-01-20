### Suppose 5 places are 1, 2, 3, 4 and 5. And you strat your trip from place 1.

- Since you may travel directly between any two places, it forms a completely connected graph as shown below:

![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/graph.png)

- Adjancency matrix for graph below 

 ![](https://github.com/JeffLoboz/DSAFINALREVIEW/blob/main/images/adjacencyMatrix.png)

Algorithm to find the cheapest trip that visit exactly 2 places is given below:

     path minTrip(int cost[][])
     {
        mincost \leftarrow 99999;

        for(i=2;i<=n;i++){

              for(j=2;j<=n;j++){

                   if(i != j && mincost > cost[1][i]+cost[i][j]+cost[j][1]){

                         mincost \leftarrow cost[1][i]+cost[i][j]+cost[j][1];

                       minpath \leftarrow (i,j);

                    }

              }

        }

        return minPath;
    }
