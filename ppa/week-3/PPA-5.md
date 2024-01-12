---
title: PPA-5
pagetitle: Week-3, PPA-5
---

## Question

Accept a sequence of positive integers as input and print the the maximum number in the sequence. The input will have $n + 1$ lines, where $n$ denotes the number of terms in the sequence. The $i^{th}$ line in the input will contain the $i^{th}$ term in the sequence for $1 \leq i \leq n$. The last line of the input will always be the number 0. Each test case will have at least one term in the sequence.

## Hint

You have to keep accepting input from the console until it is zero. Since the number of iterations is not known a priori, a `while` loop is the better choice. The next step is to accept the first input outside the while loop and store it in a variable named `t`. Now, keep accepting inputs inside the while loop. The termination condition for the loop is `t == 0`. So, keep running the loop as long as `t != 0`.

```python
t = int(input())
while t != 0:
    t = int(input())
```

With this information, can you now insert the piece of code for finding the maximum number in the sequence? You have seen it so many times in the CT course.



## Solution

```python
t = int(input())
max_t = t
while t != 0:
    if t > max_t:
        max_t = t
    t = int(input())
print(max_t)
```

