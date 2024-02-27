---
title: PPA-9
pagetitle: Week-5, PPA-9
order: 9
---

## Question

Implement the following functions:

- Write a function named **`get_column`** that accepts a matrix named `mat` and a non-negative integer named `col` as arguments. It should return the column that is at index `col` in the matrix `mat` as a list. Zero-based indexing is used here.
- Write a function named **`get_row`** that accepts a matrix named `mat` and a non-negative integer named `row` as arguments. It should return the row that is at index `row` in the matrix `mat` as a list. Zero-based indexing is used here.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the definition of both the functions.

## Hint

Such functions are extremely useful. They play the role of helper functions. When a problem is broken down into smaller parts, these helper functions will come in handy while solving the sub-problems. You should make it a point to practice writing these functions as many times as possible.

To extract a row, iterate through the columns of the matrix. Fix the row index, the first index of the matrix, and vary the column index, the second index, from $0$ to the $n - 1$, where there are $n$ columns in the matrix. A similar operation is required for extracting a column of the matrix.

## Solutions

::: {.panel-tabset}

## Solution-1

```python
def get_row(mat, row):
    row_list = [ ]
    n = len(mat[0])
    for col in range(n):
        row_list.append(mat[row][col])
	return row_list

def get_column(mat, col):
    col_list = [ ]
    m = len(mat)
    for row in range(m):
        col_list.append(mat[row][col])
    return col_list
```

## Solution-2

Since each inner list of `mat` is one row of the matrix, we can directly extract the given row by indexing into `mat`.

```python
def get_row(mat, row):
    return mat[row]

def get_column(mat, col):
    col_list = [ ]
    m = len(mat)
    for row in range(m):
        col_list.append(mat[row][col])
    return col_list
```

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/d01c9da8df334853928479c3fb200dba?sid=3493f4b4-ee90-494f-bd8b-cc328e1433cd" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
