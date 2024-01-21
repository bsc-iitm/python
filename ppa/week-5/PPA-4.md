---
title: PPA-4
pagetitle: Week-5, PPA-4
---

## Question

Write a function named **`dim_equal`** that accepts two matrices `A` and `B` as arguments. It should return `True` if the dimensions of both matrices are the same and `False` otherwise.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

Consider the following solution to this problem:

```python
def dim_equal(A, B):
    dim_A = len(A)
    dim_B = len(B)
    return dim_A == dim_B
```

Do you think this solution is correct? Does it pass all the test cases? What is it missing? For what inputs will it fail?

## Solution

::: {.panel-tabset}

## Solution-1

```python
def dim_equal(A, B):
    m_A, n_A = len(A), len(A[0])
    m_B, n_B = len(B), len(B[0])
    if (m_A == m_B) and (n_A == n_B):
        return True
   	return False
```

## Solution-2

```python
def dim_equal(A, B):
    if ((len(A) == len(B)) and 
        (len(A[0]) == len(B[0]))):
        return True
    return False
```

## Solution-3

```python
def dim_equal(A, B):
    return ((len(A) == len(B)) and
            (len(A[0]) == len(B[0])))
```

:::