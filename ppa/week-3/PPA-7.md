---
title: PPA-7
pagetitle: Week-3, PPA-7
---

## Question

Accept a positive integer as input and print the sum of the digits in the number.



## Hint

Let us take a number, say <code>1234</code> and see how to computationally approach the problem. We could start adding the digits from the left, $1 + 2 + 3 + 4$, or we could do it from the right, $4 + 3 + 2 + 1$. If we do it from the left, then we need to get hold of the leftmost digit of the number. It is not immediately clear how to do this. If we do it from the right, then we need to get hold of the last digit. Fortunately, this is something that we can easily do:

This can be done by taking the remainder when the number is divided by 10, that is, `1234 % 10 == 4`. Once we have the last digit, we no longer need it in the original number. To get rid of the last digit, we go for floor division by 10: `1234 // 10 == 123`. Now, it is just a matter of doing these two operations repeatedly:

```python
x = 1234
digit_4 = x % 10
x = x // 10
digit_3 = x % 10
x = x // 10
digit_2 = x % 10
x = x // 10
digit_1 = x % 10
```

It is now up to you to generalize this logic so that it will work for any number. Naturally, if the number of digits is arbitrary, then we have to go for a loop. Which type of loop do you think is a better option here, `for` or `while`? Are the number of iterations known a priori or not? 

If you decide to go for a while loop, what would be the termination condition? To answer the last question, think about the number $1234$ and perform the pair of operations (modulo $10$ followed by floor division by $10$) four times. What is the final value of `x` that you end up with?



## Solutions

:::{.panel-tabset}

## Solution-1

```python
n = int(input())
total = 0
while n > 0:
    total = total + (n % 10)
    n = n // 10
print(total)
```

## Solution-2

Here we retain `n` as a string and then iterate through it.

```python
n = input()
total = 0
for x in n:
    total = total + int(x)
print(total)
```

:::
