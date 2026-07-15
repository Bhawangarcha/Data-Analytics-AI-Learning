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

### 8. Combine Two Lists into a Dictionary

keys = ['a', 'b']
values = [1, 2]

d = dict(zip(keys, values))

print(d)

### Output

{'a': 1, 'b': 2}

---

### 9. Convert Tuple into Dictionary

t = ('a', 1, 'b', 2)

d = {}

for i in range(0, len(t), 2):
    d[t[i]] = t[i + 1]

print(d)

### Output

{'a': 1, 'b': 2}

---

### 10. Set Operations

A = {1, 2, 3}
B = {2, 3, 4}

print("Union:", A | B)
print("Intersection:", A & B)
print("Difference:", A - B)
print("Symmetric Difference:", A ^ B)

### Output

Union: {1, 2, 3, 4}
Intersection: {2, 3}
Difference: {1}
Symmetric Difference: {1, 4}

---

### 11. Student with Highest Marks

students = {
    "A": 80,
    "B": 92,
    "C": 75,
    "D": 88,
    "E": 90
}

name = max(students, key=students.get)

print(name, students[name])

### Output

B 92

---

### 12. Rotate List Left by n Positions

lst = [1, 2, 3, 4, 5]
n = 2

result = lst[n:] + lst[:n]

print(result)

### Output

[3, 4, 5, 1, 2]

---

### 13. Lowest Marks in Nested Dictionary

students = {
    1: {"name": "A", "marks": 70},
    2: {"name": "B", "marks": 60},
    3: {"name": "C", "marks": 80}
}

lowest = min(students.values(), key=lambda x: x["marks"])

print(lowest["name"])

### Output

B

---

### 14. Maximum and Minimum First Element

t = ((3, 'c'), (1, 'a'), (5, 'e'))

maximum = max(t)
minimum = min(t)

print("Maximum:", maximum)
print("Minimum:", minimum)

### Output

Maximum: (5, 'e')
Minimum: (1, 'a')

---

### 15. Second Largest and Second Smallest

lst = [5, 1, 9, 9, 3]

unique = sorted(set(lst))

print("Second Smallest =", unique[1])
print("Second Largest =", unique[-2])

### Output

Second Smallest = 3
Second Largest = 5

---

### 16. Unique Characters from Two Strings

s1 = "hello"
s2 = "world"

result = set(s1) | set(s2)

print(result)

### Output

{'h', 'e', 'l', 'o', 'w', 'r', 'd'}

---

### 17. Sort List of Tuples by Marks

students = [('A', 70), ('B', 90), ('C', 60)]

result = sorted(students, key=lambda x: x[1], reverse=True)

print(result)

### Output

[('B', 90), ('A', 70), ('C', 60)]

---

### 18. Merge Two Dictionaries

d1 = {'a': 1, 'b': 2}
d2 = {'b': 3, 'c': 4}

result = d1.copy()

for key, value in d2.items():
    result[key] = result.get(key, 0) + value

print(result)

### Output

{'a': 1, 'b': 5, 'c': 4}

---

### 19. Demonstrate Tuple Immutability

t = (1, 2, 3)

try:
    t[0] = 10
except TypeError:
    print("Error: tuples do not support item assignment")

### Output

---

### 20. Find Pairs Whose Sum Equals k

s = {1, 2, 3, 4, 5}
k = 6

visited = set()

for num in s:
    if k - num in s and (k - num) not in visited:
        print((num, k - num))
    visited.add(num)

### Output

(2, 4)
(1, 5)
(3, 3)

---

### 21. Sum of Diagonal Elements

matrix = (
    (1, 2, 3),
    (4, 5, 6),
    (7, 8, 9)
)

total = 0

for i in range(len(matrix)):
    total += matrix[i][i]

print("Diagonal Sum =", total)

### Output

Diagonal Sum = 15

---

### 22. Swap Keys and Values

d = {'a': 1, 'b': 2}

new_dict = {}

for key, value in d.items():
    new_dict[value] = key

print(new_dict)

### Output

{1: 'a', 2: 'b'}
