# Python Basics — For Loop, While Loop and Functions

## 🔁 For Loop

A for loop is used to repeat a block of code for a fixed number of times or to iterate over a sequence like a list, string, tuple, or range.

### Syntax:
for variable in sequence:
    statement

### Example:
for i in range(1, 6):
    print(i)

### Output:
1
2
3
4
5

### Example: Print characters of a string

name = "Python"
for ch in name:
    print(ch)

### Output:

P
y
t
h
o
n

---

### While Loop

A while loop executes a block of code repeatedly as long as the given condition is true.

### Syntax:
while condition:
    statement

### Example:
i = 1
while i <= 5:
    print(i)
    i += 1

### Output:

1
2
3
4
5

### Example: Sum of numbers
n = 5
sum = 0
i = 1
while i <= n:
    sum += i
    i += 1

print(sum)

### Output:
15

---

## Functions in Python

A function is a block of reusable code that performs a specific task. It helps reduce repetition and makes programs easier to manage.

### Syntax:
def function_name():
    statements

### Example:
def greet():
    print("Hello Python")
greet()

### Output:
Hello Python

---

### Function with Parameters

Parameters allow a function to receive values.

Example:

def add(a, b):
    print(a + b)

add(10, 20)

Output:

30

---

### Function with Return Value

A function can return a result using return.

### Example:

def square(n):
    return n * n
result = square(5)
print(result)

### Output:
25

---

### Types of Functions

### 1. Built-in Functions

Already available in Python.

### Examples:
print()
len()
input()
type()

### 2. User-defined Functions
Created by programmers using def.

### Example:
def message():
    print("Welcome")
message()

---

### Advantages of Functions:
- Code reusability
- Reduces code length
- Easy debugging
- Improves program structure
- Makes code easier to understand
