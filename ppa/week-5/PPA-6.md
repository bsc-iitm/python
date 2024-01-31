---
title: PPA-6
pagetitle: Week-5, PPA-6
order: 6
---

## Question

A class of English words is called *mysterious* if it satisfies certain conditions. These conditions are hidden from you. Instead, you are given a function named `mysterious` that accepts a word as argument and returns `True` if the word is mysterious and `False` otherwise.

<hr>

Write a function named **`type_of_sequence`** that accepts a list of words as an argument. Its return value is a string that depends on the number of mysterious words in the sequence. The exact conditions are given in the following table. If $k$ denotes the number of mysterious words in the sequence, then:

| $k$                                            | Return value          |
| ---------------------------------------------- | --------------------- |
| Less than $2$                                  | mildly mysterious     |
| Greater than or equal to $2$ but less than $5$ | moderately mysterious |
| Greater than or equal to $5$                   | most mysterious       |

You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

The takeaways from this question are twofold:

- the use of functions in expressions
- the use of function calls within other functions. 

Let us first take up a simpler example:

```python
def is_square(x):
    root = int(x ** 0.5)
    return root * root == x
```

If we want to print all square numbers in a list `L` of positive integers, this is how we would do it:

```python
# L is a list of positive integers
for elem in L:
    if is_square(elem):
        print(elem)
```

The point to note here is line-3. The function call is a part of a conditional statement. Whenever the interpreter comes across a function call, it is going to go ahead and execute that function first. Once this execution is complete, it will come back to the place from which the function was called.

`is_square(elem)` is a function call. After evaluating the function with the argument `elem`, the expression `is_square(elem)` will finally be just a Boolean value: `True` or `False`. After the function is successfully executed, the returned value is just treated like any other Python expression.

<hr>


To illustrate the second point — calling functions from within other functions — we will study the current question:

```python
def type_of_sequence(L):
    count = 0
    for word in L:
        if mysterious(word):
            count += 1
            
	## Complete the rest of the code ##
```

Note how we use the function call `mysterious(word)` inside another function `type_of_sequence`. The code snippet given above is incomplete. You have most of the information needed to complete it.

## Solution

```python
def type_of_sequence(words):
    count = 0
    for word in words:
        if mysterious(word):
            count += 1

    if count < 2:
        return 'mildly mysterious'
    elif 2 <= count < 5:
        return 'moderately mysterious'
    else:
        return 'most mysterious'
```

