# Nested Loops in Python 

## What is a Nested Loop?

A nested loop means having one loop written inside another loop.
The loop that contains another loop is called the outer loop, and the loop written inside it is called the inner loop.
### Nested loops are useful when we need to repeat an operation multiple times for every element, such as:
- Working with tables
- Printing patterns
- Handling matrices (2D lists)
- Comparing elements
- Creating combinations

### Basic Syntax:

for variable1 in sequence:
    for variable2 in sequence:
        statement

---

### How Nested Loop Works

### Example:

for i in range(3):
    for j in range(2):
        print(i, j)

### Explanation:

### Outer loop:
i = 0
i = 1
i = 2

For every value of i, the inner loop runs completely:

- When i = 0
j = 0
j = 1
- When i = 1
j = 0
j = 1
- When i = 2
j = 0
j = 1

### Output:

0 0
0 1
1 0
1 1
2 0
2 1

---

### Working of Nested Loop

Steps:
1. Outer loop starts execution.
2. Inner loop starts after every outer loop iteration.
3. Inner loop runs all its iterations.
4. After the inner loop finishes, the outer loop moves to the next value.
5. This continues until the outer loop ends.

---

### Example

for i in range(2):
    for j in range(3):
        print(f"i={i}, j={j}")

### Output:

i=0, j=0
i=0, j=1
i=0, j=2
i=1, j=0
i=1, j=1
i=1, j=2

---

### Uses of Nested Loops

### 1. Working with 2D Lists (Matrices)

A matrix is a list containing multiple lists.

### Example:

matrix = [
    [1, 2, 3],
    [4, 5, 6]
]
for row in matrix:
    for item in row:
        print(item, end=" ")

### Output:

1 2 3 4 5 6


---

### 2. Pattern Printing

Nested loops are mostly used for creating patterns.

Example:

for i in range(4):
    for j in range(i+1):
        print("*", end=" ")
    print()

### Output:

*
* *
* * *
* * * *

---

### 3. Finding Combinations

Example:

colors = ["red", "blue"]

items = ["car", "bike"]

for color in colors:
    for item in items:
        print(color, item)

Output:

red car
red bike
blue car
blue bike

Each color combines with every item.

---

### Nested Loop Using While Loop

Nested loops can also be created using while.

Example:

i = 0
while i < 3:
    j = 0
    
    while j < 2:
        print(i, j)
        j += 1
    i += 1

### Output:

0 0
0 1
1 0
1 1
2 0
2 1

---

### Using break in Nested Loop

break stops the current loop.

### Example:

for i in range(3):
    for j in range(3):
        if j == 1:
            break
        print(i,j)

### Output:

0 0
1 0
2 0

When j becomes 1, the inner loop stops.

---

### Using continue in Nested Loop

continue skips the current iteration.

Example:

for i in range(3):
    for j in range(3):
        if j == 1:
            continue
        print(i,j)

### Output:

0 0
0 2
1 0
1 2
2 0
2 2

Value j = 1 is skipped.

---

### Performance of Nested Loops

Nested loops increase execution time.

Example:

for i in range(n):
    for j in range(n):
        print(i,j)

Outer loop runs:

n times

Inner loop runs:

n times

Total:

n × n = n²

This is called Quadratic Time Complexity.

---

### Programs

- 1. Print Square Pattern

Program:

for i in range(4):
    for j in range(4):
        print("*", end=" ")
    print()

Output:

* * * *
* * * *
* * * *
* * * *


---

- 2. Right-Angled Triangle

Program:

for i in range(4):
    for j in range(i+1):
        print("*", end=" ")
    print()

Output:

*
* *
* * *
* * * *


---

- 3. Multiplication Table (1 to 5)

Program:

for i in range(1,6):
    for j in range(1,6):
        print(i,"x",j,"=",i*j)
    print()

Output:

1 x 1 = 1
1 x 2 = 2
1 x 3 = 3
...
5 x 5 = 25


---

- 4. Sum of Each Row in Matrix

Given:

matrix = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
]

Program:

for row in matrix:
    total = 0
    
    for value in row:
        total = total + value
        
    print(total)

### Output:

6
15
24


---

- 5. Count Even Numbers in 2D List

Given:

numbers = [
    [1,2,3],
    [4,6,7],
    [8,9,10]
]

Program:

count = 0

for row in numbers:
    for num in row:
        if num % 2 == 0:
            count += 1

print(count)

Output:

5

Even numbers:

2, 4, 6, 8, 10

Total:

5


---
