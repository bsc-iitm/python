---
title: PPA-9
pagetitle: Week-2, PPA-9
---

## Question

You have $n$ gold coins with you. You wish to divide this among three of your friends under the following conditions: 

1. All three of them should get a non-zero share.
2. No two of them should get the same number of coins. 
3. You should not have any coins with you at the end of this sharing process. 

The input has four lines. The first line contains the number of coins with you. The next three lines will have the share given to your three friends. All inputs shall be non-negative integers. If the division satisfies these conditions, then print the string `FAIR`. If not, print `UNFAIR`.



## Hint

There are three expressions given to you here:

```python
(a > 0) and (b > 0) and (c > 0)
(a != b) and (b != c) and (c != a)
a + b + c - n == 0
```

Now, make use of these three expressions to construct a solution. Consider another set of three expressions:

```python
(a == 0) or (b == 0) or (c == 0)
(a == b) or (b == c) or (c == a)
a + b + c - n != 0
```

Now, make use of these three expressions to construct another solution. How are these two solutions different from each other?



## Solutions

:::{.panel-tabset}

## Solution-1

```python
n = int(input())
a = int(input())
b = int(input())
c = int(input())

if (a > 0) and (b > 0) and (c > 0):
    if (a != b) and (b != c) and (c != a):
        if a + b + c - n == 0:
            print('FAIR')
        else:
            print('UNFAIR')
    else:
        print('UNFAIR')
else:
    print('UNFAIR')
```



## Solution-2

```python
n = int(input())
a = int(input())
b = int(input())
c = int(input())

flag = True
if (a == 0) or (b == 0) or (c == 0):
    flag = False
if (a == b) or (b == c) or (c == a):
    flag = False
if a + b + c - n != 0:
    flag = False

if flag:
    print('FAIR')
else:
    print('UNFAIR')
```

:::
