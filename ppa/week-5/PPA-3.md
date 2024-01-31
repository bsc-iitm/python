---
title: PPA-3
pagetitle: Week-5, PPA-3
order: 3
---

## Question

Write a function **`maxval`** that accepts three integers `a`, `b` and `c` as arguments. It should return the maximum among the three numbers.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

This function accepts three arguments and returns a single number as output. Functions can have multiple arguments and this function is an example of that. Here is a code snippet to help you solve the problem:

```python
def maxval(a, b, c):
    if (a > b) and (a > c):
        return a
```

This is obviously an incomplete solution and may even be incorrect. How will you extend this to solve the entire problem? How many return statements would you have to use if you proceed along these lines? Do you require these many return statements? Can you come up with a solution that has just one return statement?

## Solution

::: {.panel-tabset}

## Solution-1

Note that it is important to check for equality. Study what happens if all $\geq$ are changed to $>$.

```python
def maxval(a, b, c):
    if (a >= b) and (a >= c):
        return a
    elif (b >= a) and (b >= c):
        return b
	return c
```

## Solution-2

How is this different from solution-1?

```python
def maxval(a, b, c):
    maxnum = c
    if (a >= b) and (a >= c):
        maxnum = a
    elif (b >= a) and (b >= c):
        maxnum = b
	return maxnum
```

## Solution-3

Make $a$ the largest of the three numbers by swapping it with $b$ and $c$ if required. What would happen if we change the second `if` into an `elif`? We don't seem to be checking for equality here. Is that fine?

```python
def maxval(a, b, c):
    if a < b:
        a, b = b, a
    if a < c:
        a, c = c, a
    return a
```

## Solution-4

This is perhaps the simplest solution.

```python
def maxval(a, b, c):
    return max(a, b, c)
```

:::