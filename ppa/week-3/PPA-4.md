---
title: PPA-4
pagetitle: Week-3, PPA-4
---

## Question

Accept a positive integer $n$ as input, where $n > 1$. Print `PRIME` if $n$ is a prime number and `NOTPRIME` otherwise.

## Hint

There are at least two different approaches to this problem:

<u>Approach-1</u>

A prime number $p$ has exactly two factors, one and the number itself:

- $1$
- $p$

Given the number $n$ in this problem, we can count the number of factors it has. If this number is equal to $2$, then we have a prime number. This approach suggests a natural separation of the code into two parts:

- use a `for-loop` to count the number of factors of $n$ and store it in a variable, say `num`
- use an `if-else` block to check if the number of factors is equal to $2$ or not, and display the appropriate message

A variation to this approach is the following. While looping through the possible factors of $n$, if you find that the number of factors has exceeded $2$ at some stage, does it make sense to persist with the iterations? Or does it give us an opportunity to **break** out of the loop? See if you can make use of the following snippet of code:

```python
### inside some loop ###
	if num > 3:
        break
### inside some loop ###
```

Why does breaking help? What are the advantages of doing so?

<u>Approach-2</u>

A number $n$ is a composite number (not-prime) if it has a factor $f$ which is neither $1$ nor $p$. For example, $6$ is a composite number as it has a factor $2$, which is neither $1$ nor $6$. We will now use this slightly different perspective to solve the problem.

This approach is based on the idea of the **state** of a system. In our case, the system is the code. In most problems in our course, the `state` will be binary. For this problem, we will associate prime numbers with `state = True`. Therefore, while looping through the factors of $n$, we could be in one of these two states:

- `state = True`
- `state = False`

If the `state` is `True`, it means that *so far* we have not come across any factor of $n$ other than $1$ and $n$. The moment we find a factor of $n$ other than $1$ and $n$, we should update the `state` to `False`. For example:

```python
state = True
for f in range(1, n + 1):
    if (n % f == 0) and (f != 1) and (f != n):
        state = False
```

We start with an "optimistic" mindset that the number $n$ is a prime and set `state = True` in line-1. During the looping process, if we find that $n$ is composite, we update the `state` to `False`. If $n$ is indeed prime, then the `state` remains `True` even after the loop ends. Either way, at the end of the loop, the `state` variable will tell us whether the number $n$ is prime or not. Notice that the `state` is a dynamic entity during the looping process. For a composite number, `state = True` to begin with, but it eventually becomes `False`. 

This approach is an extremely powerful template and can be applied to a wide range of problems. We will refer to this as the **state-approach** in future problems where this is used. There are some variants to this solution as well. Does breaking out of the loop make sense here? If the `state` become `False`, can it ever become `True` again? Finally, is there a simpler way of writing the if-condition so that we don't have to check for three conditions? The hint lies in rethinking about the range of numbers that you have to check for. Should it be `range(1, n + 1)`, or can it be something else?



## Solutions

:::{.panel-tabset}

## Solution-1

```python
n = int(input())

for f in range(1, n + 1):
    if n % f == 0:
        count += 1
if count == 2:
    print('PRIME')
else:
    print('NOTPRIME')
```



## Solution-2

```python
n = int(input())
# optimistic start
is_prime = True

for f in range(1, n + 1):
    if (n % f == 0) and (f != 1) and (f != n):
        is_prime = False
        break

if is_prime:
    print('PRIME')
else:
    print('NOTPRIME')
```





## Solution-3

Though the following code will not work for $n = 1$, the question states that $n > 1$. We have made use of this fact. This code is a slight improvement over solution-2.

```python
n = int(input())
# optimistic start
is_prime = True

for f in range(2, n):
    if n % f == 0:
        is_prime = False
        break

if is_prime:
    print('PRIME')
else:
    print('NOTPRIME')
```

:::
