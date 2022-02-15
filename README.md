# DP-QUESTION-NOV-BRAVE-BATCH-2022

Fibonacci number -> The Fibonacci Sequence is the series of numbers:

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...

The next number is found by adding up the two numbers before it:

the 2 is found by adding the two numbers before it (1+1),
the 3 is found by adding the two numbers before it (1+2),
the 5 is (2+3),
and so on!
#code in java
//leetcode link->https://leetcode.com/problems/fibonacci-number/
```
import java.util.*;
public class Main{
    public int fib(int n) {
        int dp[]=new int[n+1];
        return fibnacciDP(n,dp);
    }
    
    public static int fibnacciDP(int n,int dp[]){
        if(n==0 || n==1){
            return n;
        }
        
        if(dp[n]!=0){
            return dp[n];
        }
        
        int x=fibnacciDP(n-1,dp);
        int y=fibnacciDP(n-2,dp);
        int sum = x+y;
        dp[n]=sum;
        return sum;
    }
}
```

//EXAMPLE format
Input: n = 2
Output: 1
Explanation: F(2) = F(1) + F(0) = 1 + 0 = 1.
Input: n = 3
Output: 2
Explanation: F(3) = F(2) + F(1) = 1 + 1 = 2.
