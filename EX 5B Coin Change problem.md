# EX 5B Coin Change Problem

## DATE: 06.05.2025

## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm

1. Start the program.
2. Define a function coinChange(coins, amount).
3. Initialize a list dp of size amount + 1 with all values as infinity (float('inf')).
4. Set dp[0] = 0 since zero coins are needed to make amount 0.
5. Loop through each coin in the coins list.
6. For each coin, iterate from coin to amount.
7. Update dp[i] = min(dp[i], dp[i - coin] + 1) to get the minimum coins for amount i.
8. After all loops, check if dp[amount] is still infinity.
9. If yes, return -1 because the amount cannot be formed with the given coins. Otherwise, return dp[amount] as the fewest number of coins needed.
10. End the program.



## Program:

```
Create a python function to compute the fewest number of coins that we need to make up the amount given.
Developed by: SATHYAA R
Register Number: 212223100052
```

```
class Solution(object):
    def coinChange(self, coins, amount):
        dp = [float('inf')] * (amount + 1)
        dp[0] = 0  

        for coin in coins:
            for i in range(coin, amount + 1):
                dp[i] = min(dp[i], dp[i - coin] + 1)
        return dp[amount] if dp[amount] != float('inf') else -1
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))
print(ob1.coinChange(s,amt))
```


## Output:

![image](https://github.com/user-attachments/assets/b223a79e-a04f-476a-8804-1a0e6ef08a40)


## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
