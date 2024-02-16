---
title: PPA-8
pagetitle: Week-4, PPA-8
order: 8
---

## Question

An identity matrix is a square matrix which has ones on the main diagonal and zeros everywhere else. For example, the identity matrix of size $3 \times 3$ is:
$$
\begin{bmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{bmatrix}
$$

<hr>

Accept a positive integer $n$ as input and print the identity matrix of size $n \times n$. Your output should have $n$ lines, where each line is a sequence of $n$ comma-separated integers that corresponds to one row of the matrix.



## Hint

In order to print the elements of a matrix with one row on each line, a nested loop is needed. After the inner loop goes through a row, a new line should be added. This can be done with a simple `print` statement.

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for i in range(3):
    for j in range(3):
        print(matrix[i][j], end = ',')
    print()
```

This gives the following output:

```python
1,2,3,
4,5,6,
7,8,9,
```

How does one get rid of the comma at the end? Check out [PPA-5](/ppa/week-4/PPA-5.md) to get the logic for this.



## Solution

```python
n = int(input())
I = [ ]
for i in range(n):
    row = [ ]
    for j in range(n):
        if i == j:
            row.append(1)
        else:
            row.append(0)
    I.append(row)
    
for i in range(n):
    for j in range(n):
        if j != n - 1:
            print(I[i][j], end = ',')
        else:
            print(I[i][j])
```

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/3d37ca67c029487db741398d4c1228f4?sid=7acc133e-9efb-43fd-917f-869f1d68f9dc" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
