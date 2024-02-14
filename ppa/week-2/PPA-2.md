---
title: PPA-2
pagetitle: Week-2, PPA-2
order: 2
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

Notice the usage `0 < x < 10`. This is called operator chaining. This actually corresponds to `0 < x and x < 10`. We have *chained* two operations into a single one. Chaining enables us to smoothly translate the mathematical expression $0 < x < 10$ to the Python expression `0 < x < 10`.

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

## Solution-5

This is the last variation. Instead of having `elif`, we have an `if` in both places. This is also a valid solution for this problem. This is because the conditions in the two if-blocks are mutually exclusive. That is, if $0 < x < 10$, then the body of the first if-block gets executed. There is no way for the second if-block also to get triggered since $10 \leq x$ will evaluate to false.

```python
x = float(input())
y = 0.0
if 0 < x < 10:
    y = x + 2
if 10 <= x:
    y = x ** 2 + 2
print(y)
```

It is better to stick to `if-elif-else` ladders wherever possible and avoid a sequence of `if` conditions. The `if-elif-else` ladder is more efficient. As soon as one of the conditions is satisfied, the control will exit from the ladder. An `if-if-if` ladder on the other hand will end up checking every one of the `if` conditions for every possible input.

:::

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/274c940c1fe6435eb7191851dfa36b90?sid=a31d8d8d-c4c1-4aaa-8bd5-e9b5b324f1a9" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
