# Python Practice Questions

### 1. Check whether two sets are disjoint

set1 = {1, 2}
set2 = {3, 4}

print(set1.isdisjoint(set2))

### Output:

True

---

### 2. Flatten a nested list

nested = [[1, 2], [3, [4, 5]], 6]

def flatten(lst):
    result = []
    for item in lst:
        if isinstance(item, list):
            result.extend(flatten(item))
        else:
            result.append(item)
    return result

print(flatten(nested))

### Output:

[1, 2, 3, 4, 5, 6]

---

### 3. Remove dictionary values less than a threshold

d = {'a': 5, 'b': 15, 'c': 2}
threshold = 10

result = {}
for key, value in d.items():
    if value >= threshold:
        result[key] = value

print(result)

### Output:

{'b': 15}

---

### 4. Count occurrences in a tuple without count()

t = (1, 2, 2, 3, 2, 4)
value = 2

count = 0
for i in t:
    if i == value:
        count += 1

print(count)

### Output:

3

---

### 5. Merge two lists and sort in descending order (without sort() or sorted())

list1 = [3, 1, 5]
list2 = [2, 8]

merged = list1 + list2

for i in range(len(merged)):
    for j in range(i + 1, len(merged)):
        if merged[i] < merged[j]:
            merged[i], merged[j] = merged[j], merged[i]

print(merged)

### Output:

[8, 5, 3, 2, 1]

---

### 6. Demonstrate sets cannot contain mutable elements

try:
    s = {[1, 2], 3}
except TypeError as e:
    print("Error:", e)

### Output:

Error: unhashable type: 'list'

---

### 7. Sum of tuple elements at even indices

t = (10, 20, 30, 40, 50)

total = 0
for i in range(0, len(t), 2):
    total += t[i]

print(total)

### Output:

90

---

### 8. Check key exists, otherwise add default value

d = {'a': 1}
key = 'b'
default = 0

if key not in d:
    d[key] = default

print(d)

### Output:

{'a': 1, 'b': 0}

---

### 9. Find sum, average, maximum and minimum without built-in functions

lst = [4, 8, 1, 9, 3]

total = 0
maximum = lst[0]
minimum = lst[0]

for i in lst:
    total += i
    if i > maximum:
        maximum = i
    if i < minimum:
        minimum = i

average = total / len(lst)

print("Sum =", total)
print("Average =", average)
print("Maximum =", maximum)
print("Minimum =", minimum)

### Output:

Sum = 25
Average = 5.0
Maximum = 9
Minimum = 1

---

### 10. Find unique characters from two strings

s1 = "hello"
s2 = "world"

result = set(s1) | set(s2)

print(result)

### Output:

{'h', 'e', 'l', 'o', 'w', 'r', 'd'}

---

### 11. Sort list of tuples by marks (descending)

students = [('A', 70), ('B', 90), ('C', 60)]

for i in range(len(students)):
    for j in range(i + 1, len(students)):
        if students[i][1] < students[j][1]:
            students[i], students[j] = students[j], students[i]

print(students)

### Output:

[('B', 90), ('A', 70), ('C', 60)]

---

### 12. Merge two dictionaries by summing common values

d1 = {'a': 1, 'b': 2}
d2 = {'b': 3, 'c': 4}

result = d1.copy()

for key, value in d2.items():
    if key in result:
        result[key] += value
    else:
        result[key] = value

print(result)

### Output:

{'a': 1, 'b': 5, 'c': 4}

---

### 13. Demonstrate tuple immutability

t = (1, 2, 3)

try:
    t[0] = 10
except TypeError:
    print("Error: tuples do not support item assignment")

### Output:

Error: tuples do not support item assignment

---

### 14. Find pairs whose sum equals target

s = {1, 2, 3, 4, 5}
k = 6

for num in s:
    if (k - num) in s and num < (k - num):
        print((num, k - num))

### Output:

(1, 5)
(2, 4)

---

### 15. Sum of diagonal elements in a 3×3 matrix

matrix = (
    (1, 2, 3),
    (4, 5, 6),
    (7, 8, 9)
)

total = 0

for i in range(len(matrix)):
    total += matrix[i][i]

print(total)

### Output:

15

---

### 16. Swap keys and values of a dictionary

d = {'a': 1, 'b': 2}

swapped = {}

for key, value in d.items():
    swapped[value] = key

print(swapped)

### Output:

{1: 'a', 2: 'b'}

---

### 17. Find unique words ignoring case and punctuation

import string

sentence = "Hi! Hi, how are you?"

sentence = sentence.lower()

for ch in string.punctuation:
    sentence = sentence.replace(ch, "")

words = sentence.split()

print(set(words))

### Output:

{'hi', 'how', 'are', 'you'}

---

### 18. Check subset and superset

set1 = {1, 2}
set2 = {1, 2, 3}

print("Subset:", set1.issubset(set2))
print("Superset:", set2.issuperset(set1))

### Output:

Subset: True
Superset: True
