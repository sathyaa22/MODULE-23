# EX 5D Minimum Jump to Reach End Array

## DATE: 09.05.2025

## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm

1. Start the program.
2. If the array is empty (n == 0) or the first element is 0, return infinity (float('inf')) because the end can't be reached.
3. Create a list jumps[] of size n to store the minimum jumps needed to reach each index.
4. Initialize jumps[0] = 0 since 0 jumps are needed to stay at the first position.
5. For each index i from 1 to n - 1, set jumps[i] = inf initially.
6. For each i, loop through all previous indices j from 0 to i - 1.
7. If index i is reachable from j (i.e., i <= j + arr[j]) and jumps[j] is not infinity, then:
    Update jumps[i] = min(jumps[i], jumps[j] + 1).
8. Break the inner loop once a valid jump is found for that i.
9. After all loops, return jumps[n - 1] as the minimum number of jumps to reach the end.
10. End the program.


## Program:
```
To implement the program to finding the minimum number of jumps needed to
reach end of the array.
Developed by: SATHYAA R
Register Number: 212223100052
```

```
def minJumps(arr, n):
    jumps = [0 for i in range(n)]
    if (n == 0) or (arr[0] == 0):
        return float('inf')
 
    jumps[0] = 0
    for i in range(1, n):
        jumps[i] = float('inf')
        for j in range(i):
            if (i <= j + arr[j]) and (jumps[j] != float('inf')):
                jumps[i] = min(jumps[i], jumps[j] + 1)
                break
    return jumps[n-1]
    
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
```


## Output:

![image](https://github.com/user-attachments/assets/c757989f-8154-4686-bcf4-7f92a2f7ff21)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
