---
title: PPA-7
pagetitle: Week-5, PPA-7
---

## Question

In a throwback to CT days, write the definition of the following five functions, all of which accept a list L as argument.

- **`is_empty`**: return `True` if the list is empty, and `False` otherwise.

- **`first`**: return the first element if the list is non-empty, return `None` otherwise.
- **`last`**: return the last element if the list is non-empty, return `None` otherwise.
- **`init`**: return the first $n - 1$ elements if the list is non-empty and has size $n$, return `None` otherwise. Note that if `L` has just one element, `init(L)` should return the empty list.
- **`rest`**: return the last $n - 1$ elements if the list is non-empty and has size $n$, return `None` otherwise. Note that if `L` has just one element, `rest(L)` should return the empty list.

<hr>

You do not have to accept input from the user or print output to the console. You just have to write the definition of all the five functions. Each test case corresponds to one function call.

## Hint

We will go one function at a time:

- `is_empty`: We are going to write three different solutions for this:

<u>Solution-1</u>

```python
def is_empty(L):
    if L == [ ]:
        return True
    else:
        return False
```

<u>Solution-2</u>

```python
def is_empty(L):
    if L == [ ]:
        return True
	return False
```

<u>Solution-3</u>

```python
def is_empty(L):
    return L == [ ]
```

Are all three solutions correct? Which one do you think is better?

- `first`: there are again three solutions that we will look at:

<u>Solution-1</u>

```python
def first(L):
    if L == [ ]:
        return None
    else:
        return L[0]
```

<u>Solution-2</u>

```python
def first(L):
    if L == [ ]:
        return None
   	return L[0]
```

<u>Solution-3</u>

Here, we are assuming that `is_empty` is available to us.

```python
def first(L):
    if is_empty(L):
        return None
    return L[0]
```

Again, look at these three solutions and try to identify which one is better.

- `last`

Is the following solution correct? If not, what do you think is wrong with it?

```python
def last(L):
    return L[-1]
```

- `init`

```python
def init(L):
    if L == [ ]:
        return None
	out = [ ]
    n = len(L)
    for x in range(n - 1):
        out.append(x)
    return out
```

Is there a simpler solution that doesn't require the explicit creation of a new list `out`?

- `rest`

This is similar to the previous function. We just need to leave out the first element and include the rest.

## Solution

```python
def is_empty(L):
    return L == [ ]

def first(L):
    if is_empty(L):
        return None
    return L[0]

def last(L):
    if is_empty(L):
        return None
    return L[-1]

def init(L):
    if is_empty(L):
        return None
    return L[:-1]

def rest(L):
    if is_empty(L):
        return None
    return L[1: ]
```

