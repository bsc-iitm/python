---
title: PPA-8
pagetitle: Week-2, PPA-8
---

## Question

Consider the following image of a chess-board (image borrowed from [chess.com](https://www.chess.com/terms/chess-bishop)). The piece on the board is a bishop.

![](../assets/images/img_001.png){width=50%; fig-align=center}

Accept two positions as input: `start` and `end`. Print **YES** if a bishop at `start` can move to `end` in exactly one move. Print **NO** otherwise. Note that a bishop can only move along diagonals.



## Hint

The bishop is capable of only diagonal moves. In the problem statement, you have to figure out if the bishop can move from `start` to `end` in exactly one move. So you have to see if this movement is along a diagonal or not. What are the characteristics of a diagonal? In terms of coordinate geometry, what is the slope of a diagonal?

As far as the inputs are concerned, each position on the chessboard is given by two symbols: a letter and a number. The letter denotes the column and the number denotes the row. For example, the bishop in the image given above is at `C4`. In the test cases, we use capital letters for the columns.

Now consider the following strings:

```python
cols = 'ABCDEFGH'
rows = '12345678'
```

And the following snippet of code:

```python
cols.index('D')
```

Can you come up with the solution using these hints?

## Solution

```python
start = input()
end = input()

cols = 'ABCDEFGH'
rows = '12345678'

start_col, start_row = start
end_col, end_row = end

col_diff = cols.index(start_col) - cols.index(end_col)
row_diff = rows.index(start_row) - rows.index(end_row)

# abs(x) returns the absolute value of x
if abs(col_diff) == abs(row_diff):
    print('YES')
else:
    print('NO')
```

