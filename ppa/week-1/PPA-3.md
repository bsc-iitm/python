---
title: PPA-3
pagetitle: Week-1, PPA-3
---

## Question

Accept an integer as input and print its square as output.

## Hint

The `input` function always returns a string. If you want to accept an integer from the console, you have to first accept a string and then convert it into an integer:

```python
word = input()
x = int(word)	# x is now an integer
```

You could of course do it in a single line as:

```python
x = int(input())
```

Do not get confused between the exponentiation and the multiplication operator:

- `*`: multiplication
- `**`: exponentiation



## Solution

There is a trivial difference between the two solutions. Solution-1 introduces an intermediate variable, `y`, which represents the square of `x` and then prints it. Solution-2 does away with this intermediate variable and directly prints the square of `x`.

:::{.panel-tabset}

## Solution-1

```python
x = int(input())
y = x ** 2
print(y)
```

## Solution-2

```python
x = int(input())
print(x ** 2)
```

:::
