---
title: PPA-2
pagetitle: Week-2, PPA-2
---

## Question

Consider the piece-wise function given below.

$$
f(x) = \left\{
        \begin{array}{ll}
            x + 2 & \quad 0 < x < 10 \\
            x^2 + 2 & \quad 10 \leq x \\
            0 & \quad \text{otherwise}
        \end{array}
    \right.
$$

Accept the value of $x$ as input and print the value of $f(x)$ as output. Note that both the input and output are real numbers. Your code should reflect this aspect. That is, both $x$ and $f(x)$ should be float values.

## Hint

Real numbers are represented as `float` values. So, you would have to accept the input as follows:

```python
x = float(input())
```

The output in this case is the value of $f(x)$, which is again to be treated as a float value according to the question. Here is an incomplete code snippet that you can use to complete the solution:

```python
if 0 < x < 10:
    print(x + 2)
```

Notice the usage `0 < x < 10`. This is called operator chaining. This actually corresponds to `0 < x and x < 10`. We have *chained* two operations into a single one. This chaining enables us to smoothly translate from the mathematical expression $0 < x < 10$ to the Python expression `0 < x < 10`.

Few more things to consider:

- If you use `print` statements within the conditional blocks, like the way it is shown here, how many of them would you require to solve this problem?
- Is there a way to solve this problem that requires just one `print` statement? Can you come up with that solution if it exists?

## Solutions

You have to be careful about printing the value $0$. The expected value is $0.0$, the float value, and not $0$, the integer value.

::: {.panel-tabset}

## Solution-1

```python
x = float(input())
if 0 < x < 10:
    print(x + 2)
elif 10 <= x:
    print(x ** 2 + 2)
else:
    print(0.0)
```

## Solution-2

```python
x = float(input())
if 0 < x < 10:
    y = x + 2
elif 10 <= x:
    y = x ** 2 + 2
else:
    y = 0.0
print(y)
```

## Solution-3

Here is a slight variation of solution-2. Can you see what has changed?

```python
x = float(input())
y = 0.0
if 0 < x < 10:
    y = x + 2
elif 10 <= x:
    y = x ** 2 + 2
print(y)
```

## Solution-4

This is different from all three solutions before. Instead of using operator chaining, this uses the `and` operator:

```python
x = float(input())
y = 0.0
if 0 < x and x < 10:
    y = x + 2
elif 10 <= x:
    y = x ** 2 + 2
print(y)
```



:::
