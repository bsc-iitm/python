---
title: PPA-10
pagetitle: Week-5, PPA-10
order: 10
---

## Question

Write a function **`insert`** that accepts a sorted list `L` of integers and an integer `x` as arguments. The function should return a sorted list with the element `x` inserted at the right place in the input list. The original list should not be disturbed in the process.

<hr>

- The only built-in methods you are allowed to use are append and remove. You should not use any other method provided for lists.
- You do not have to accept input from the user or print output to the console. You just have to write the function definition.

## Hint

For a moment, forget that this is a problem about functions. How do you approach a problem like this? 

<u>Step-1</u>

We are not deleting any elements from the input list. Clearly, the output list should have all the elements in the input list. So, let us write the skeleton of that code:

```python
out = [ ]
for elem in L:
    out.append(elem)
```

<u>Step-2</u>

Now, we need to decide when to insert an element `x`. We start from the smallest element at the left-end of the list and keep going right. If `x` is less than the current `elem`, then this is the right place to insert `x`. Remember that this works only if `L` is sorted.

```python
out = [ ]
for elem in L:
    if x < elem:
        out.append(x)
    out.append(elem)
```

This seems to be a good place to stop. It looks as though we have solved the problem. So, let us just wrap this up in a function:

```python
def insert(L, x):
    out = [ ]
    for elem in L:
        if x < elem:
            out.append(x)
        out.append(elem)
    return out
```

When we test-run this code, we find that it fails the second test case:

```python
out = insert([1, 3, 7, 10, 20], 8)
print(out)	# -> [1, 3, 7, 8, 10, 8, 20]
```

The element $8$ is inserted twice. So, this code is wrong, or at least incomplete. To fix this, we need to keep track of the insertion process. Once an element is inserted, we need some way of signaling that we need not insert it again. Secondly, let us run the following code and see what happens:

```python
out = insert([1, 3, 7, 10, 20], 22)
print(out)	# -> [1, 3, 7, 10, 20]
```

The element $22$ was not even inserted! This is the second problem with the current code. It is now left to you to figure out how to address these two deficiencies with the current solution.

## Solution

We maintain the state of the code in the Boolean variable `inserted`. This variable will remain `False` as long as `x` is not inserted into `L`. We iterate through through each `elem` of the list and check for two conditions:

- `inserted == False`
- `x < elem`

If both conditions evaluate to `True`, then this is the right place to insert `x`. We insert it here and update `inserted` to `True`. It may so happen that `inserted` never becomes `True` even after iterating through all the elements in the list. This could happen in two situations:

- `x` is the larger than the maximum element in `L`
- `L` is empty

In both these cases, we have to get outside the loop and check if `x` has been inserted or not. If not, we have to insert it at the end of the output list.

```python
def insert(L, x):
    out = [ ]
    inserted = False
    for elem in L:
        if (not inserted) and (x < elem):
            inserted = True
            out.append(x)
        out.append(elem)
    if not inserted:
        out.append(x)
    return out
```

