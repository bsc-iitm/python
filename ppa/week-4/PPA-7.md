---
title: PPA-7
pagetitle: Week-4, PPA-7
---

## Question

Accept a square matrix as input and store it in a variable named `matrix`.  The first line of input will be, $n$, the number of rows in the matrix. Each of the next $n$ lines will have a sequence of $n$ space-separated integers.



## Hint

How does one accept a row of a matrix?

A row of input is usually provided as a sequence of numbers:

```
1 2 3 4 5
```

PPAs 1 to 6 should give you the idea here.

```python
nums = input().split(' ')	# split by space
row = [ ]					# represents one row of a matrix
for num in nums:
    row.append(int(num))	# convert str to int
```

Now, you just need to append this row to another list `matrix`:

```python
matrix = [ ]
matrix.append(row)
print(matrix)
```

Your matrix currently has only one row in it and would look like this:

```python
[[1, 2, 3, 4, 5]]
```

Now it is just a question of using a loop to append all rows of a matrix to the outer list `matrix` one by one. For the first test case, this is what happens:

```python
matrix = [ ]
# Row-1: 1 2
row = [1, 2]
matrix.append(row)
# Matrix becomes [[1, 2]]
# Row-2: 3 4
row = [3, 4]
matrix.append(row)
# Matrix becomes [[1, 2], [3, 4]]
```

Now, loopify!



## Solution

```python
n = int(input())

matrix = [ ]
for _ in range(n):
    row = [ ]
    for num in input().split(' '):
        row.append(int(num))
    matrix.append(row)
```



