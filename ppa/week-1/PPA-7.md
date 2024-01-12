---
title: PPA-7
pagetitle: Week-1, PPA-7
---

## Question

Accept a five digit number as input and print the sum of its digits as output.



## Hint

Sometimes, it may be more beneficial to accept a string as input and not convert it into an integer right away.

```python
x = input()
first = int(x[0])
```

What do you think the variable `first` contains in the above snippet of code? Do you see how you can extend this idea to solve the problem?

As a second approach, we can start with $x$ as an integer. Instead of processing the number from left to right, let us try to process it from right to left. How do we get the last digit of a number? The last digit is the remainder when the number is divided by $10$:

```python
last = x % 10
```

Once we have the last digit, we no longer need it. So, we need to remove it from $x$. How do we do it? We can do floor division by $10$:

```python
x = x // 10
```

Can you complete the solution?



## Solutions

::: {.panel-tabset}

## Solution-1

```python
x = input()
first = int(x[0])
second = int(x[1])
third = int(x[2])
fourth = int(x[3])
fifth = int(x[4])
print(first + second + third + fourth + fifth)
```



## Solution-2

```python
x = int(input())
fifth = x % 10
x = x // 10
fourth = x % 10
x = x // 10
third = x % 10
x = x // 10
second = x % 10
x = x // 10
first = x % 10
print(first + second + third + fourth + fifth)
```

:::
