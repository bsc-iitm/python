---
title: Docstrings
pagetitle: Docstrings
---

All the function-templates that we provide the solution area in the portal have what is called a doc-string associated with them. The doc-string is a description of what the function is supposed to do. In our course, the doc string has three elements:

- one line description of the function
- arguments accepted by the function
- return value of the function

For example:

```python
def factorial(n):
    """
    computes the factorial of an integer
    
    Argument:
        n: integer
    Return:
        result: integer
    """
    # start writing code from here
```

We have seen students start populating the function before the doc-string. This is not a good practice. In the above example, the doc-string ends at line-9. The body of the function should start from line-10 and not prior to that. Also, the doc-string is not mandatory. You can go ahead and delete it. The function would still work.