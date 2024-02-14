---
title: PPA-2
pagetitle: Week-3, PPA-2
order: 2
---

## Question

Accept a positive integer $n$ as input and print all the factors of $n$, one number on each line.



## Hint

Given a number $n$, a number $f$ is its factor if $n$ is divisible by $f$. We know that $n$ is divisible by $f$  if the remainder when $n$ is divided by $f$ is $0$. In Python, we have the $\%$ operator for getting the remainder:

```python
if n % f == 0:
    print('a factor')
else:
    print('not a factor')
```

The above snippet is of course just checking if a number $f$ is a factor of $n$ or not. Use the key idea in this snippet to come up with a complete solution to this problem. What is the `range` of values that you will have to check for $f$, the loop-variable in this case?

An important point concerning the choice of variable names. `i` or `j` as the name for a loop variable is too generic for most problems. Reserve `i` and `j` for indices of strings and lists (we will study this next week). For this problem, `f` is a good choice because we need to find the **f**actors of a number. The loop variable could also have more descriptive names, two of which are given below:

- `fact`
- `factor`

At the same time, avoid excessively long names. For example, `factor_of_n` is unnecessarily elaborate. Note that any valid variable name would do and would give the same output, but in the interest of writing readable code, we strongly urge you to be a little more mindful in picking "good" names.

## Solution

```python
n = int(input())
for f in range(1, n + 1):
    if n % f == 0:
        print(f)
```



## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/80a30f23ee26410f8e6b613c5e24884a?sid=7113a9fe-9307-4b35-9d92-1cea010e493d" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
