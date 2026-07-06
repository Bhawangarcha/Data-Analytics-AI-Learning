# NumPy (Numerical Python)

## What is NumPy?

NumPy (Numerical Python) is an open-source Python library used for performing fast numerical computations and working with multi-dimensional arrays. It is one of the most important libraries in Python for scientific computing.
NumPy provides a powerful N-dimensional array object (ndarray) and a large collection of mathematical functions to perform operations on these arrays efficiently.
NumPy is the foundation of many Python libraries such as Pandas, SciPy, Matplotlib, TensorFlow, and Scikit-learn.

---

### Why Do We Need NumPy?

Python lists are useful, but they have some limitations:
- They are slower for numerical calculations.
- They consume more memory.
- Mathematical operations require loops.

### NumPy solves these problems by:

- Performing operations much faster.
- Using less memory.
- Allowing element-wise operations without writing loops.
- Supporting multidimensional arrays.

### Advantages of NumPy

- Fast execution (implemented in C language internally)
- Less memory usage
- Easy mathematical operations
- Supports vectorization (operations without loops)
- Useful in Data Science, AI, Machine Learning, Image Processing, and Scientific Computing

---

### Features of NumPy

- Supports one-dimensional, two-dimensional, and multidimensional arrays.
- Provides hundreds of built-in mathematical functions.
- Supports array indexing and slicing.
- Allows reshaping and combining arrays.
- Generates random numbers.
- Performs statistical and linear algebra operations.
- Compatible with many Python libraries.

---

### Installing NumPy

- If NumPy is not installed, install it using pip.
- pip install numpy

 ### To use NumPy in a Python program:

import numpy as np
Here np is an alias (short name) for NumPy.

---

### 1. Creating Arrays

An array is a collection of elements of the same data type stored together in memory.
Unlike Python lists, NumPy arrays are optimized for numerical calculations.

### 1D Array

A one-dimensional array is similar to a list.

import numpy as np

arr = np.array([1,2,3,4])
print(arr)

### Output

[1 2 3 4]

---

### 2D Array

A two-dimensional array consists of rows and columns.

arr2 = np.array([[1,2],
                 [3,4]])

print(arr2)

### Output

[[1 2]
 [3 4]]

---

### 2. Array Attributes

Every NumPy array has several useful properties called attributes.

arr = np.array([[1,2,3],
                [4,5,6]])

print(arr.ndim)
print(arr.shape)
print(arr.size)
print(arr.dtype)

### Output

2
(2,3)
6
int64

---

### 3. Special Arrays

NumPy provides functions to quickly create commonly used arrays.

---

- Zeros Array

Creates an array where every element is 0.

print(np.zeros((2,3)))

### Output

[[0. 0. 0.]
 [0. 0. 0.]]

Used when initializing data.

---

- Ones Array

Creates an array filled with 1.

print(np.ones((3,3)))

### Output

[[1. 1. 1.]
 [1. 1. 1.]
 [1. 1. 1.]]

---

-  Identity Matrix

An identity matrix is a square matrix where:

diagonal elements are 1

remaining elements are 0


print(np.eye(3))

### Output

[[1.0 0.0 0.0]
 [0.0 1.0 0.0]
 [0.0 0.0 1.0]]

Used in Linear Algebra.

---

- arange()

Creates numbers within a specified range.

print(np.arange(1,10,2))

### Output

[1 3 5 7 9]

### Syntax

np.arange(start, stop, step)

---

- linspace()

Creates equally spaced numbers.

print(np.linspace(0,1,5))

### Output

[0.   0.25 0.50 0.75 1.00]

Syntax

np.linspace(start, stop, number_of_values)


---

### 4. Array Operations

Theory

Unlike Python lists, NumPy performs operations element by element.

a = np.array([1,2,3])
b = np.array([4,5,6])

print(a+b)
print(a-b)
print(a*b)
print(a/b)

Output

[5 7 9]
[-3 -3 -3]
[4 10 18]
[0.25 0.4 0.5]

These operations are called vectorized operations, making NumPy very fast.


---

### 5. Mathematical Functions

NumPy contains many built-in mathematical functions.

arr = np.array([1,4,9])

print(np.sqrt(arr))
print(np.sum(arr))
print(np.mean(arr))
print(np.max(arr))
print(np.min(arr))

### Output

[1. 2. 3.]
14
4.666666666666667
9
1

---

### 6. Indexing and Slicing

Indexing is used to access individual elements.

Slicing is used to access multiple elements.

arr = np.array([10,20,30,40])

print(arr[0])
print(arr[-1])

### Output

10
40

Negative indexing starts from the end.


---

### Slicing

print(arr[1:3])

### Output

[20 30]

Syntax

array[start:end]

The ending index is not included.

---

### 7. Reshaping Arrays

Reshaping changes the structure of an array without changing its data.

arr = np.array([1,2,3,4,5,6])

new_arr = arr.reshape(2,3)

print(new_arr)

### Output

[[1 2 3]
 [4 5 6]]

The total number of elements must remain the same.

---

### 8. Iterating Through Arrays

Arrays can be traversed using loops.

arr = np.array([1,2,3])

for x in arr:
    print(x)

### Output

1
2
3

Each iteration accesses one element of the array.

---

### 9. Copy vs View

Copy

A copy creates a completely separate array.

Changes in the original array do not affect the copied array.

arr = np.array([1,2,3])

x = arr.copy()

arr[0] = 10

print(arr)
print(x)

### Output

[10 2 3]
[1 2 3]

---

### View

A view shares the same memory as the original array.

Changes made in one array appear in the other.

arr = np.array([1,2,3])

y = arr.view()

arr[0] = 10

print(arr)
print(y)

### Output

[10 2 3]
[10 2 3]

---

### 10. Joining Arrays

Joining combines two or more arrays into one array.

a = np.array([1,2])
b = np.array([3,4])

print(np.concatenate((a,b)))

### Output

[1 2 3 4]

---

### 11. Sorting Arrays

Sorting arranges array elements in ascending order.

arr = np.array([3,1,2])

print(np.sort(arr))

### Output

[1 2 3]

---

### 12. Random Numbers

NumPy provides a random module to generate random numbers.

random_arr = np.random.randint(1,10,5)

print(random_arr)

### Output

[3 7 1 9 5]

Each execution gives different values.

---

### 13. Boolean Filtering

Boolean filtering selects only those elements that satisfy a condition.

arr = np.array([1,2,3,4,5])

print(arr[arr>2])

### Output

[3 4 5]

Only elements greater than 2 are returned.

---

### Summary

NumPy is one of the most important Python libraries for numerical computing. It provides efficient multidimensional arrays, fast mathematical operations, array manipulation, random number generation, sorting, filtering, reshaping, and statistical functions. Because of its speed, memory efficiency, and extensive functionality, NumPy serves as the foundation for many advanced fields such as Data Science, Machine Learning, Artificial Intelligence, Image Processing, and Scientific Computing. Mastering NumPy is an essential step toward learning these technologies effectively.
