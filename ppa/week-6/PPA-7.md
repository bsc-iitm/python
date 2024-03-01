---
title: PPA-7
pagetitle: Week-6, PPA-7
order: 7
---

## Question

In this problem, we shall try to create the list of dictionaries with was given to us in the previous problem.

<hr>

Accept a positive integer $n$ that represents the number of students in the class. $n$ blocks of input follow. Each block is made up of six lines and contains the details of one student in the class. Create a dictionary corresponding to each student. All keys should be strings. The type of the value corresponding to a key and the order in which the inputs should be accepted are shown in the table given below:

| Line number | Key         | Type of Value |
| ----------- | ----------- | ------------- |
| 1           | Name        | String        |
| 2           | City        | String        |
| 3           | SeqNo       | Integer       |
| 4           | Mathematics | Integer       |
| 5           | Physics     | Integer       |
| 6           | Chemistry   | Integer       |

Append each dictionary to a list named `scores_dataset`. This is the list that we will finally use for evaluating your code. The dictionaries corresponding to the students should be appended in the order in which they appear in the sequence of inputs.

<hr>

You do not have to print the output to the console.

## Hint

We will look at one block of input:

```python
name = input()
city = input()
seqno = int(input())
math = int(input())
phy = int(input())
chem = int(input())

student = dict()
student['Name'] = name
student['City'] = city
student['SeqNo'] = seqno
student['Mathematics'] = math
student['Physics'] = phy
student['Chemistry'] = chem
```

Be careful about the types of the inputs. If a variable is specified as integer, be doubly careful about converting the input into an integer.

## Solution

Long dictionaries with several key-value pairs can be written across multiple lines as shown in this snippet of code. Note that lines 12-14 are the key-value pairs of the dictionary `student`.

```python
n = int(input())

scores_dataset = [ ]

for _ in range(n):
    name = input()
    city = input()
    seqno = int(input())
    math = int(input())
    phy = int(input())
    chem = int(input())
    student = {
        'Name': name, 'City': city,
        'SeqNo': seqno, 'Mathematics': math,
        'Physics': phy, 'Chemistry': chem
    }
    scores_dataset.append(student)
```



