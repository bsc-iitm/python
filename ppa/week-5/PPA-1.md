---
title: PPA-1
pagetitle: Week-5, PPA-1
---

## Question

The factorial is a positive integer $n$ is the product of the first $n$ positive integers.

<hr>

Write a function named **`factorial`** that accepts an integer `n` as argument. It should return the factorial of `n` if `n` is a positive integer. It should return $-1$ if `n` is a negative integer, and it should return $1$ if `n` is zero.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

The main takeaway from this problem is the way functions behave when there are multiple return statements. Let us take a simpler example to begin with. 

```python
def odd_even(n):
    if n % 2 == 0:
        return 'even'
    return 'odd'
```

In any function that has multiple return statements, exactly one of them will be executed. The moment a return statement is executed, control exits from the function. The function `odd_even` given above has two return statements. When $n$ is even, the return statement in line-3 will be executed. If $n$ is not even, then the return statement in line-4 will be executed. Now, we come to the `factorial` function. This has three return statements. The body of the function is simple enough and you should be able to fill it.

## Solution

```python
def factorial(n):
    if n < 0:
        return -1
    if n == 0:
        return 1
    fact = 1
    for x in range(1, n + 1):
        fact = fact * x
    return fact
```

Notice the type of function. This function has a single argument and single return value.