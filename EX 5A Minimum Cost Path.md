# EX 5A Minimum Cost Path

## DATE: 06.05.2025

## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.


## Algorithm

1. Start the program.
2. Read the number of rows R and columns C from the user.
3. The cost matrix is a 2D list that contains the cost of each cell.
4. Base Case 1: If m < 0 or n < 0, return a very large value (infinity). This handles invalid indexes.
5. Base Case 2: If the destination is the starting cell (0, 0), return its cost cost[0][0].
6. Recursive Case: Return the cost of the current cell cost[m][n] plus the minimum of the three possible previous cells:
7. Define a Helper Function min(x, y, z). This returns the minimum of the three given values.
8. Create a sample cost matrix and call minCost(cost, m, n) with the target cell coordinates.
9. Display the minimum cost to reach the destination cell.
10. End the program.

  

## Program:
```
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.
Developed by: SATHYAA R
Register Number: 212223100052
```

```
R=int(input())
C=int(input())
import sys
def minCost(cost, m, n):
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
    minCost(cost, m-1, n),
    minCost(cost, m, n-1) )
    
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
        
cost= [ [1, 2, 3],
 [4, 8, 2],
 [1, 5, 3] ]
print(minCost(cost, 2, 2))
```


## Output:

![image](https://github.com/user-attachments/assets/ffeef142-5ff7-4c64-92aa-105102cd3d3c)


## Result:
Thus the above program was executed successfully for finding the minimum cost.
