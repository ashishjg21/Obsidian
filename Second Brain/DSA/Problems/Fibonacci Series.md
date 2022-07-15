
## Fibonacci Series
[todo- binets fibonacci formula](https://r-knott.surrey.ac.uk/Fibonacci/fibFormula.html)
### Solution 1 - Recursive Approach

Time Complexity - O(2^N)  
Space Complexity - O(N) given the function call stack size

```
    int fib(int N) {
        if(N == 0)  return 0;
        if(N == 1)  return 1;
        return fib(N-1) + fib(N-2);
    }
```

### Solution 2 - Dynamic Programming Approach

Use memoization to store perviously computed fibonacci values.  
****Time Complexity - O(N)  
Space Complexity - O(N)

```
    int fib(int N) {
        if(N < 2)
            return N;
        int memo[N+1];
        memo[0] = 0;
        memo[1] = 1;
        for(int i=2; i<=N; i++)
            memo[i] = memo[i-1] + memo[i-2];
        return memo[N];
    }
```

### Solution 3 - Imperative Approach (Bottom Up DP)

With Imperative approach, we step through the loop and optimize the space by storing only two previous fibonacci values in two variables.  
****Time Complexity - O(N)  
Space Complexity - O(1)

```
    int fib(int N) {
        if(N < 2) 
            return N;
    	int a = 0, b = 1, c = 0;
        for(int i = 1; i < N; i++)
        {
            c = a + b;
            a = b;
            b = c;
        }
        return c;
    }
```

### Solution 4 - Binet's Nth-term Formula

Using Binet's Formula for the Nth Fibonacci involves the usage of our golden section number **Phi**.  
**Phi** = ( sqrt(5) + 1 ) / 2  
Using approximation equation is good enough here, since we know N >= 0 && N <= 30, we can safely use the following rounded function  
Fib(N) = round( ( **Phi**^N ) / sqrt(5) )  
Full mathematical explanation of Binet's Formula [here](http://www.maths.surrey.ac.uk/hosted-sites/R.Knott/Fibonacci/fibFormula.html)  
****Time Complexity - O(1)  
Space Complexity - O(1)

```
    int fib(int N) {
        double phi = (sqrt(5) + 1) / 2;     
        return round(pow(phi, N) / sqrt(5));
    }
```

