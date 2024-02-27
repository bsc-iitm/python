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

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/73113a595c6f49748dd39d7f3e8d520b?sid=0ecf5078-e957-4af9-948d-4550e637d2de" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
