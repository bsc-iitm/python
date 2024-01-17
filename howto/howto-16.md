---
title: Print all elements in a list on the same line separated by a comma
pagetitle: How-to
sidebar: false
---

```python
L = ['this', 'is', 'a', 'sentence']
for word in L:
    print(word, end = ',')
```

This will add a comma after every word. As a result, there will be a comma after the last word. To get rid of it we can use this snippet:

```python
L = ['this', 'is', 'a', 'sentence']
for word in L[:-1]:
    print(word, end = ',')
print(L[-1])
```

This iterates through the first $n - 1$ entries in the list of length $n$. The last element is printed outside the loop. The code is agnostic to the type of the values inside the list. That is, this snippet would work for a list of integers or a list of float values as well.

If we are dealing with a list of strings, there is a smarter way of doing this:

```python
L = ['this', 'is', 'a', 'sentence']
sentence = ','.join(L)
print(sentence)
```

`join` is a string method that accepts a list of strings as argument and joins the elements in the list by using comma (the string on which the method is called) as the separator. If `join` is called using a different string, say a space, then the separator would be different.