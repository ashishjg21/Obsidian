
https://github.com/ashishjg21/Random-Number-Generator

**Linear Congruential Method** is a class of (Pseudo Random Number Generator (PRNG)](https://www.geeksforgeeks.org/pseudo-random-number-generator-prng/) algorithms used for generating sequences of random-like numbers in a specific range. This method can be defined as: 

X_{i + 1} = a(X_{i}) + c  mod m    
where,

X, is the sequence of pseudo-random numbers
m, ( > 0) the modulus
a, (0, m) the multiplier
c, (0, m) the increment
X0,  [0, m) – Initial value of sequence known as seed

m, a, c, and X0 should be chosen appropriately to get a period almost equal to m. 

 where, 
 **X,** is the sequence of pseudo-random numbers  
 **m,** ( > 0) the modulus  
 **a,** (0, m) the multiplier  
 **c,** (0, m) the increment  
**X0**, 0, m) – Initial value of sequence known as seed 
 m, a, c, and X0 should be chosen appropriately to get a period almost equal to m. 

For a = 1, it will be the additive congruence method.  
For c = 0, it will be the multiplicative congruence method. 

**Approach:** 

-   Choose the seed value X0, Modulus parameter m, Multiplier term a, and increment term c.
-   Initialize the required amount of random numbers to generate (say, an integer variable _noOfRandomNums_).
-   Define a storage to keep the generated random numbers (here, _vector_ is considered) of size _noOfRandomNums_.
-   Initialize the 0th index of the vector with the seed value.
-   For rest of the indexes follow the Linear Congruential Method to generate the random numbers.

> randomNums[i] = ((randomNums[i – 1] * a) + c) % m 

Finally, return the random numbers.
