---
title: PPA-11
pagetitle: Week-3, PPA-11
order: 11
---

## Question

Accept a positive integer $n$ as input and find all solutions to the equation:
$$
x^2 + y^2 = z^2
$$
subject to the following constraints:

(1) $x$, $y$ and $z$ are positive integers

(2) $x < y < z < n$

Print each solution triplet on one line — `x,y,z` — with a comma between consecutive integers. The triplets should be printed in ascending order. If you do not find any solutions satisfying the given constraints, print the string `NO SOLUTION` as output.

<u>Order relation among triplets</u>

Given two triplets $T_1 = (x_1, y_1, z_1)$ and $T_2 = (x_2, y_2, z_2)$, use the following process to compare them:

(1) If $x_1 < x_2$, then $T_1 < T_2$

(2) If $x_1 = x_2$ and $y_1 < y_2$, then $T_1 < T_2$

(3) If $x_1 = x_2$, $y_1 = y_2$, and $z_1 < z_2$, then $T_1 < T_2$



## Hint

First, study the following snippet of code:

```python
for x in range(1, 3):
    for y in range(1, 3):
        for z in range(1, 3):
            print(x, y, z)
```

This is the output:

```default
1 1 1
1 1 2
1 2 1
1 2 2
2 1 1
2 1 2
2 2 1
2 2 2
```

What can you say about the order in which the triplets are printed? How will you use this idea to construct a solution to this problem?

## Solution

```python
n = int(input())

num = 0
for x in range(1, n):
    for y in range(x + 1, n):
        for z in range(y + 1, n):
            if x ** 2 + y ** 2 == z ** 2:
                print(f'{x},{y},{z}')
                num += 1
if num == 0:
    print('NO SOLUTION')
```

