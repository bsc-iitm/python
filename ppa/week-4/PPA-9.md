---
title: PPA-9
pagetitle: Week-4, PPA-9
---

## Question

Accept a square matrix $A$ and an integer $s$ as input and print the matrix $s \cdot A$ as output. Multiplying a matrix by an integer $s$ is equivalent to multiplying each element of the matrix by $s$. For example:
$$
2 \cdot \begin{bmatrix}
1 & 2\\
3 & 4
\end{bmatrix} = \begin{bmatrix}
2 & 4\\
6 & 8
\end{bmatrix}
$$

<hr>
The first line of input is a positive integer, $n$, that denotes the dimension of the matrix $A$. Each of the next $n$ lines contains a sequence of space-separated integers. The last line of the input contains the integer $s$.

Print the matrix $s \cdot A$ as output. Each row of the matrix must be printed as a sequence of space separated integers, one row on each line. There should not be any space after the last number on each line.

## Hint

One way to do it is to accept the matrix $A$ as input and then create a new matrix $B$, such that:
$$
B[i][j] = s \cdot A[i][j]
$$

```python
B = [ ]
n = len(A)
for i in range(n):
    row = [ ]
    for j in range(n):
        row.append(s * A[i][j])
    B.append(row)
```

Though this forms a part of a valid solution, is there another way of solving this problem?



## Solution

```python
n = int(input())
matrix = [ ]
for i in range(n):
    row = [ ]
    for x in input().split(' '):
        row.append(int(x))
    matrix.append(row)
s = int(input())

for i in range(n):
    for j in range(n):
        matrix[i][j] *= s

for i in range(n):
    for j in range(n):
        if j != n - 1:
            print(matrix[i][j], end = ' ')
        else:
            print(matrix[i][j])
```

