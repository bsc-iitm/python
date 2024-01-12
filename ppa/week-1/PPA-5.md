---
title: PPA-5
pagetitle: Week-1, PPA-5
---

## Question

Accept two words as input and print the two words after adding a space between them.



## Hint

String concatenation is a good place to start:

```python
first = 'one'
second = 'two'
print(first + second)
```

The output is:

```default
onetwo
```

How do you modify the code so that there is a space between `one` and `two`? This is something for you to think about.



## Solutions

::: {.panel-tabset}

## Solution-1

```python
first = input()
second = input()
space = ' ' # there is one space between the quotes
out = first + space + second
print(out)
```

## Solution-2

The `print` function adds space as a default separator when multiple arguments are passed to it.

```python
first = input()
second = input()
print(first, second)
```

## Solution-3

Here, we are explicitly specifying the separator to be space.

```python
first = input()
second = input()
print(first, second, sep = ' ') # one space between the quotes
```

:::
