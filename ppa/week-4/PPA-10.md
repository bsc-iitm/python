---
title: PPA-10
pagetitle: Week-4, PPA-10
order: 10
---

## Question

Accept two square matrices $A$ and $B$ of dimensions $n \times n$ as input and compute their sum $A + B$.

<hr>

The first line will contain the integer $n$. This is followed by $2n$ lines. Each of the first $n$ lines is a sequence of comma-separated integers that denotes one row of the matrix $A$. Each of the last $n$ lines is a sequence of comma-separated integers that denotes one row of the matrix $B$. Your output should again be a sequence of $n$ lines, where each line is a sequence of comma-separated integer that denotes a row of the matrix $A + B$.



## Hint

This may be one of the longest snippets that you would have to write. While writing this code, note the redundancy involved. You have to accept two matrices as input, so you would have two sets of nested loops, both of which are almost identical in appearance. How can you avoid this redundancy? We will learn functions in week-5 which will solve this problem.

That said, once you have two matrices $A$ and $B$ in place, you need a new matrix $C$ such that:
$$
C[i][j] = A[i][j] + B[i][j]
$$



## Solution

```python
n = int(input())

A = [ ]
for i in range(n):
    row = [ ]
    for x in input().split(','):
        row.append(int(x))
    A.append(row)
    
B = [ ]
for i in range(n):
    row = [ ]
    for x in input().split(','):
        row.append(int(x))
    B.append(row)
    
C = [ ]
for i in range(n):
    row = [ ]
    for j in range(n):
        row.append(0)
    C.append(row)
    
for i in range(n):
    for j in range(n):
        C[i][j] = A[i][j] + B[i][j]
        if j != n - 1:
            print(C[i][j], end = ',')
        else:
            print(C[i][j])
```

