# EX 5C Kadane's Algorithm

## DATE: 09.05.2025

## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm

1. Start the program.
2. Define a function maxSubArraySum(a, size).
3. Initialize max_till_now as the first element of the array a[0].
4. Initialize max_ending as 0 to keep track of the current subarray sum.
5. Loop from index 0 to size - 1.
6. Add the current element a[i] to max_ending.
7. If max_ending < 0, reset max_ending to 0.
8. If max_ending is greater than max_till_now, update max_till_now = max_ending.
9. After the loop, return max_till_now as the maximum contiguous subarray sum.
10. End the program.


## Program:
```
To implement the program to find the maximum contiguous subarray.
Developed by: SATHYAA R
Register Number: 212223100052
```

```
def maxSubArraySum(a,size):
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```


## Output:

![image](https://github.com/user-attachments/assets/ec4aeb06-9845-46c5-b619-4249a84e3dbc)


## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray.
