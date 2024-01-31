---
title: PPA-8
pagetitle: Week-5, PPA-8
order: 8
---

## Question

Write a recursive function named **`fibo`** that accepts a positive integer $n$ as argument and returns the $n^{\text{th}}$ Fibonacci number. For this problem, $F_1 = F_2 = 1$ are the first two Fibonacci numbers.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

Every recursive function has two parts:

- recursive call
- base case

If $F_n$ is the $n^{th}$ Fibonacci number, we have:
$$
F_n = F_{n - 1} + F_{n - 2}
$$
In Pythonic terms, if $\text{fibo}$ is a Python function that returns the $n^{th}$ Fibonacci number, then, we can express it as:
$$
\text{fibo}(n - 1) + \text{fibo}(n - 2)
$$
This is what $\text{fibo}(n)$ should return and will be our recursive call. The base case of the recursion is based on the fact that $F_1 = F_2 = 1$. This is done using a simple if-condition. 

## Solution

```python
def fibo(n):
    if n <= 2:
        return 1
    return fibo(n - 1) + fibo(n - 2)
```

