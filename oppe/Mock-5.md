---
title: Mock-5
pagetitle: Mock-5
order: 5

---

## Video Solution

<div style="position: relative; padding-bottom: 53.43750000000001%; height: 0;"><iframe src="https://www.loom.com/embed/ad2e9b8d56c34200a8cb3d992c57cf55?sid=d21994a3-858a-46f9-b611-d349219fff6d" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Solution

A smaller solution is possible if we only look at a $3 \times 3$ board. The following solution ended up being this long because we have considered a general $n \times n$ tic-tac-toe board.

```python
def row_pattern(board, r):
    return board[r]
    
def col_pattern(board, c):
    L = [ ]
    for i in range(len(board)):
        L.append(board[i][c])
    return L
            
def main_diag_pattern(board):
    L = [ ]
    for i in range(len(board)):
        L.append(board[i][i])
    return L
    
def anti_diag_pattern(board):
    L = [ ]
    for i in range(len(board)):
        L.append(board[i][-i-1])
    return L

def tic_tac_toe(board):
    patterns = [ ]
    for i in range(len(board)):
        patterns.append(row_pattern(board, i))
        patterns.append(col_pattern(board, i))
    patterns.append(main_diag_pattern(board))
    patterns.append(anti_diag_pattern(board))
        
    for pattern in patterns:
        if pattern == ['X'] * len(board):
            return 'X'
        elif pattern == ['O'] * len(board):
            return 'O'
    return -1
```

