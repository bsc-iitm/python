---
title: PPA-10
pagetitle: Week-3, PPA-10
---

## Question

Accept a positive integer $n$ as input and print the sum of all prime numbers in the range $[1, n]$, endpoints inclusive. If there are no prime numbers in the given range, then print 0.



##  Hint

You already know how to find if a number is prime or not. This was discussed in the tutorials and you must have solved an earlier PPA related to this same subject. Now, all that you need is a nested loop, where you go over all numbers in the given range, check if each one is a prime or not, and just add those numbers that are primes.

## Solution

```python
n = int(input())
total = 0

for i in range(2, n + 1):
    is_prime = True
    for j in range(2, i):
        if (i % j == 0):
            is_prime = False
            break
    if is_prime:
        total = total + i
    
print(total)
```

