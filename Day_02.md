# Daily Dairy Day_02
# Python
##  Topics learned
- Variables and data types
- Numeric data types (int, float)
- String data type and string operations
- String Methods
- Type casting
- Cinditional statements
- Nested if Condition

## Introduction To Python

Python is a high-level, interpreted, object-oriented, and general-purpose programming language. It was created by Guido Van Rossum and first in 1991.
Python is popular because:
- It has simple and rwadable syntax.
- It requires fewer lines of code compared many other languages.
- It supports multiple programming approaches like procedural, object-oriented, and functional programming.
- It has a large collection of built in libraries.
### Python is used in:
- Wenb development
- Data Science
- Aritificial Intelligence
- Machine Learning
- Automation
- GAme development
- Software development

## Variable

A variable is a name used to store a value in the computer's memory. It works like a container that holds data which can be used later in a program.
In Python, we do not need to declare the variable type. Python automatically detects the type of value stored. This is called dynamic typing.

Example:
name = "Bhawandeep"
age = 20
marks = 85.5
print(name)
print(age)
print(marks)

### Output:
Bhawandeep
20
85.5

Here:
- name stores a string value
- age stores an integer value
- marks stores a float value

---

### Creating Variables

### Syntax:
variable_name = value

### Example:

x = 10
y = 5
sum = x + y
print(sum)

### Output:

15
---

### Variable Value Can Change

A variable's value can be updated during program execution.

### Example:

age = 18
print(age)
age = 20
print(age)

### Output:

18
20
---

### Multiple Variables

Python allows assigning multiple variables at once.

### Example:

a, b, c = 10, 20, 30
print(a)
print(b)
print(c)

### Output:

10
20
30
---

### Rules for Naming Variables

### 1. Variable name must start with a letter or underscore.

- Correct:
student = "Ram"
_student = "Ram"

- Incorrect:
1student = "Ram"

---

### 2. Variable names cannot contain spaces.

- Correct:
student_name = "Ram"

- Incorrect:
student name = "Ram"

---

### 3. Python keywords cannot be used as variable names.

Incorrect:

if = 10

---

## Types of Variables

### 1. Local Variable

A variable created inside a function.

### Example:

def test():
    x = 10
    print(x)
test()
x is a local variable.

---

### 2. Global Variable

A variable created outside a function.

Example:
x = 50
def show():
    print(x)
show()
x can be used throughout the program.

---

### Checking Variable Type
type() function is used to check the data type.

### Example:

x = 10
print(type(x))

### Output:

<class 'int'>
---

## Numeric Data Types (int and float)

Numeric data types are used to store numbers in a program. They are mainly used for calculations and mathematical operations.
Python has two commonly used numeric data types:

### 1. int (Integer)
### 2. float (Floating Point Number)
---

### 1. Integer (int)
An integer is a whole number without a decimal point.
It can store:
- Positive numbers
- Negative numbers
- Zero

### Examples:
age = 20
marks = 95
temperature = -10

### Example Program:

a = 10
b = 5
print(a + b)
print(a - b)
print(a * b)
print(a // b)

### Output:
15
5
50
2

---

### 2. Float (float)

A float is a number that contains a decimal point. It is used when we need more accurate values.

Examples:

price = 99.99
height = 5.8
percentage = 87.5

### Example:

x = 10.5
y = 2.5
print(x + y)
print(x / y)

### Output:
13.0
4.2

--

### Checking Data Type

x = 10
y = 5.5

print(type(x))
print(type(y))

Output:

<class 'int'>
<class 'float'>

---

### Type Conversion

### int to float

x = 10
print(float(x))

### Output:
10.0

### float to int
x = 5.8
print(int(x))

### Output:
5

---
### String Data Type

A string is a sequence of characters stored inside single quotes (' '), double quotes (" "), or triple quotes (''' ''').
Strings are used to store text data like names, messages, sentences, etc.

### Examples:
name = "Bhawandeep"
city = 'Ludhiana'
message = """Hello Python"""

Here:
- name stores a string
- city stores a string

message stores a multi-line string

---

## String Properties

### 1. Strings are Immutable

Strings cannot be changed after they are created.

### Example:
text = "Python"
text[0] = "J"

### Output:
Error

Because strings cannot be modified directly.

---

### String Indexing

Each character in a string has a position called an index.

### Example:
word = "Python"
print(word[0])
print(word[3])

### Output:
P
h

### Index starts from 0.

P  y  t  h  o  n
0  1  2  3  4  5


---

### String Operations

String operations are used to perform different tasks on strings.

---

### 1. Concatenation (+)
Joining two or more strings is called concatenation.

### Example:

first = "Hello"
second = "Python"
result = first + " " + second
print(result)

### Output:
Hello Python

---

### 2. Repetition (*)
Repeating a string multiple times.

### Example:
text = "Hi "
print(text * 3)

### Output:
Hi Hi Hi

---

### 3. String Length (len())

len() is used to find the number of characters.

### Example:
name = "Python"
print(len(name))

### Output:
6

---

### 4. String Slicing

Slicing is used to get a part of a string.

### Syntax:
string[start:end]

### Example:
word = "Python"
print(word[0:3])

### Output:
Pyt

---

### 5. Membership Operators
- Used to check whether a word or character exists in a string.
- in

### Example:
text = "Python"
print("P" in text)

### Output:
True
not in

### Example:
print("Java" not in text)

### Output:
True

---

### 6. String Comparison

Strings can be compared using:

- ==
- !=
- >
- <

### Example:

a = "Python"
b = "Python"
print(a == b)

### Output:
True

---

### 7. Changing Case

- Uppercase

text = "python"
print(text.upper())

### Output:
PYTHON

- Lowercase
text = "PYTHON"
print(text.lower())

### Output:
python

---

### Example Program

name = input("Enter name: ")
print("Hello " + name)
print("Length:", len(name))

### Output:
Enter name: Bhawan
Hello Bhawan
Length: 6

---
