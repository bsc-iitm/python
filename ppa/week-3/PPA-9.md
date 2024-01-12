---
title: PPA-9
pagetitle: Week-3, PPA-9
---

## Question

Accept a positive integer $n$ as input and print a triangle of zeros for $n$ lines. The $i^{th}$ line should have $i$ zeros. There shouldn't be any spaces between consecutive zeros. Do not print a space at the end of a line.



## Hint

Nested loops are one way to solve the problem. What should be the ranges for the outer and inner for loops? How many rows are we printing? In each row, how many zeros are we printing? To move to the next row, just use `print()`.

But there is also a way to solve the problem using a single loop. A hint is given below:

- string
- integer
- multiplication

How can you use a combination of the three terms mentioned here to construct a solution?



## Solution

```python
n = int(input())
for i in range(1, n + 1):
    for j in range(1, i + 1):
        print('0', end = '')
    print()
```

