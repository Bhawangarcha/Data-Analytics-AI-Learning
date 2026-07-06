# Practice questions

---

### 1. Remove duplicates and return a sorted list

lst = [4, 1, 4, 2, 3, 1]

result = sorted(set(lst))

print(result)

### Output

[1, 2, 3, 4]

---

### 2. Find the frequency of each element

lst = ['a', 'b', 'a', 'c', 'b', 'a']

freq = {}

for i in lst:
    freq[i] = freq.get(i, 0) + 1

for key, value in freq.items():
    print(f"{key}: {value}")

### Output

a: 3
b: 2
c: 1

---

### 3. Sort a dictionary by values

d = {'a': 3, 'b': 1, 'c': 2}

result = sorted(d.items(), key=lambda x: x[1])

print(result)

### Output

[('b', 1), ('c', 2), ('a', 3)]

---

### 4. Swap two tuples

a = (1, 2)
b = (3, 4)

a, b = b, a

print("a =", a)
print("b =", b)

### Output

a = (3, 4)
b = (1, 2)

---

### 5. Separate even and odd numbers

lst = [1, 2, 3, 4, 5, 6]

even = []
odd = []

for i in lst:
    if i % 2 == 0:
        even.append(i)
    else:
        odd.append(i)

print("Even =", even)
print("Odd =", odd)

### Output
Even = 2, 4, 6
Odd = 1, 3, 5

---

### 6. Common elements among three sets

a = {1, 2, 3}
b = {2, 3, 4}
c = {2, 3, 5}

print(a & b & c)

### Output

{2, 3}

---

### 7. Tuple unpacking

t = (1, 2, 3, 4, 5)

a, b, c, d, e = t
print(a, b, c, d, e)

first, *rest = t
print(first)
print(rest)


---

8. Combine two lists into a dictionary

keys = ['a', 'b']
values = [1, 2]

d = dict(zip(keys, values))

print(d)


---

16. Convert tuple into dictionary

t = ('a', 1, 'b', 2)

d = {}

for i in range(0, len(t), 2):
    d[t[i]] = t[i + 1]

print(d)


---

17. Set operations

A = {1, 2, 3}
B = {2, 3, 4}

print("Union:", A | B)
print("Intersection:", A & B)
print("Difference:", A - B)
print("Symmetric Difference:", A ^ B)


---

18. Student with highest marks

students = {
    "A": 80,
    "B": 92,
    "C": 75,
    "D": 88,
    "E": 90
}

name = max(students, key=students.get)

print(name, students[name])


---

19. Rotate list left by n positions

lst = [1, 2, 3, 4, 5]
n = 2

result = lst[n:] + lst[:n]

print(result)


---

20. Lowest marks in nested dictionary

students = {
    1: {"name": "A", "marks": 70},
    2: {"name": "B", "marks": 60},
    3: {"name": "C", "marks": 80}
}

lowest = min(students.values(), key=lambda x: x["marks"])

print(lowest["name"])


---

21. Maximum and minimum first element

t = ((3, 'c'), (1, 'a'), (5, 'e'))

maximum = max(t)
minimum = min(t)

print("Maximum:", maximum)
print("Minimum:", minimum)


---

22. Second largest and second smallest

lst = [5, 1, 9, 9, 3]

unique = sorted(set(lst))

print("Second Smallest =", unique[1])
print("Second Largest =", unique[-2])


---

32. Unique characters from two strings

s1 = "hello"
s2 = "world"

result = set(s1) | set(s2)

print(result)


---

33. Sort list of tuples by marks

students = [('A', 70), ('B', 90), ('C', 60)]

result = sorted(students, key=lambda x: x[1], reverse=True)

print(result)


---

34. Merge two dictionaries

d1 = {'a': 1, 'b': 2}
d2 = {'b': 3, 'c': 4}

result = d1.copy()

for key, value in d2.items():
    result[key] = result.get(key, 0) + value

print(result)


---

35. Demonstrate tuple immutability

t = (1, 2, 3)

try:
    t[0] = 10
except TypeError:
    print("Error: tuples do not support item assignment")


---

36. Find pairs whose sum equals k

s = {1, 2, 3, 4, 5}
k = 6

visited = set()

for num in s:
    if k - num in s and (k - num) not in visited:
        print((num, k - num))
    visited.add(num)


---

37. Sum of diagonal elements

matrix = (
    (1, 2, 3),
    (4, 5, 6),
    (7, 8, 9)
)

total = 0

for i in range(len(matrix)):
    total += matrix[i][i]

print("Diagonal Sum =", total)

Output

Diagonal Sum = 15


---

38. Swap keys and values

d = {'a': 1, 'b': 2}

new_dict = {}

for key, value in d.items():
    new_dict[value] = key

print(new_dict)

Output

{1: 'a', 2: 'b'}

These solutions use fundamental Python concepts such as lists, tuples, sets, dictionaries, loops, conditions, zip(), sorted(), max(), min(), lambda functions, and exception handling, making them suitable for lab practicals and examinations.
