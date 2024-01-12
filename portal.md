# Portal

Certain instructions:

- An important point to note is the sensitiveness of the portal to the kind of output that you produce. If the expected output is $7.0$, then the actual output should also be $7.0$. If you print $7$, that would turn out to be a wrong answer, even though it may be mathematically correct. This is because, the portal does a strict string-matching between the output that you produce **(actual output)** and the configured output **(expected output)**. To see how strict the comparison is, try to add a space after the number that you are expected to print. Though you won't be able to see the space in the actual output area, the portal will call it a wrong answer. This is because, the space is an extra character and is not present in the configured answer.
- Another thing to avoid is the following:

```python
x = float(input('Enter a real number:'))
```

**Avoid** passing a string into the `input` command while coding on the portal. This string gets printed in the actual output area, which would result in a wrong answer.