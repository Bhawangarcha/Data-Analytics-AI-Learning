## List Operations in Python 

### 1. What is a List?

A list is a collection of multiple values stored in a single variable. Lists can store different types of data.

my_list = [1, 2, 3, 4]

### Properties of List:

- Ordered: Items maintain their position.
- Mutable: Elements can be changed after creation.
- Allows duplicates: Same value can appear multiple times.


### Example:
numbers = [10, 20, 20, 30]

---

### 2. Accessing Elements

Indexing

Index is used to access individual elements.

my_list = [10, 20, 30, 40]
print(my_list[0])   # First element
print(my_list[-1])  # Last element

### Output:
10
40

- Slicing

Used to access a range of elements.

my_list[1:3]

Output:
[20, 30]

---

### 3. Adding Elements

- append()

Adds an element at the end of the list.

my_list = [1,2,3]
my_list.append(4)
print(my_list)

### Output:
[1,2,3,4]

---

- insert()

Adds an element at a specific index.

my_list.insert(1,10)

Output:
[1,10,2,3]

---

- extend()

Adds multiple elements.

my_list.extend([5,6,7])

### Output:
[1,2,3,5,6,7]

---

### 4. Removing Elements

- remove()

Removes a specific value.

my_list.remove(2)

---

- pop()

Removes element using index.

my_list.pop()

Removes last element.

my_list.pop(1)

Removes element at index 1.

---

- clear()

Removes all elements.

my_list.clear()

### Output:
[]

---

### 5. Updating Elements

List values can be changed because lists are mutable.

my_list = [10,20,30]
my_list[0] = 100
print(my_list)

### Output:
[100,20,30]

---

### 6. List Operations

- Concatenation (+)

Combines two lists.

a = [1,2]
b = [3,4]
print(a+b)

### Output:

[1,2,3,4]

---

- Repetition (*)

Repeats list elements.

a = [1,2]
print(a*3)

### Output:

[1,2,1,2,1,2]

---

### 7. Membership Operators

Checks whether an element exists.

my_list = [1,2,3]

print(2 in my_list)
print(5 not in my_list)

### Output:

True
True

---

### 8. Length of List

len() returns number of items.

my_list = [10,20,30]
print(len(my_list))

### Output:
3

---

### 9. Sorting Lists

sort()

Changes original list.

- Ascending:

numbers = [4,1,3,2]
numbers.sort()
print(numbers)

### Output:

[1,2,3,4]

- Descending:

numbers.sort(reverse=True)

### Output:

[4,3,2,1]

---

### sorted()

Creates a new sorted list.

new_list = sorted(numbers)

---

### 10. Reverse List

Reverses the order.

my_list.reverse()

### Example:

- Before:

[1,2,3]

- After:

[3,2,1]

---

### 11. Looping Through List

Used to access every element.

my_list = [10,20,30]
for item in my_list:
    print(item)

### Output:

10
20
30

---

### 12. List Comprehension

Short method to create lists.

### Example:

squares = [x*x for x in range(5)]
print(squares)

### Output:

[0,1,4,9,16]

---

### 13. Built-in Functions

- Minimum value

min(my_list)

- Maximum value

max(my_list)
Sum of elements
sum(my_list)

### Example:
numbers = [1,2,3]
print(sum(numbers))

### Output:
6

---

### 14. Copying Lists

Creates a separate copy of a list.

my_list = [1,2,3]
new_list = my_list.copy()
print(new_list)

### Output:
[1,2,3]

---

### Example Program

numbers = [5,2,8,1]
numbers.append(10)
numbers.sort()
for i in numbers:
    print(i)

### Output:
1
2
5
8
10

---

## Tuple Operations in Python

### 1. What is a Tuple?

A tuple is a collection of multiple items stored in a single variable.

t = (1, 2, 3)

### Properties of Tuple:

- Ordered: Elements keep their position.
- Immutable: Values cannot be changed after creation.
- Allows duplicates: Same values can appear multiple times.
- Faster than lists for accessing data.

### Example:
t = (10, 20, 20, 30)

---

### 2. Creating a Tuple

- Normal Tuple

t = (1, 2, 3)

- Parentheses Optional

t2 = 4, 5, 6

- Single Element Tuple

A comma is required:

single = (10,)

Without comma it is considered an integer.

---

### 3. Accessing Elements

- Indexing

t = (10,20,30,40)
print(t[0])

### Output:
10

- Negative Indexing

print(t[-1])

### Output:
40

- Slicing

print(t[1:3])

### Output:
(20,30)

---

### 4. Tuple Operations

### 1. Concatenation (+)

Combines two tuples.

t1 = (1,2)
t2 = (3,4)
print(t1+t2)

### Output:
(1,2,3,4)

---

### 2. Repetition (*)

Repeats tuple elements.

t = (1,2)
print(t*3)

### Output:
(1,2,1,2,1,2)

---

### 3. Membership Test

Checks if an element exists.

t = (1,2,3)
print(2 in t)
print(5 not in t)

### Output:
True
True

---

### 5. Built-in Functions

- len()

Returns number of elements.

t = (4,2,8,1)
print(len(t))

### Output:
4

---

- max()

Finds maximum value.

print(max(t))

### Output
8

---

- min()

Finds minimum value.

print(min(t))

### Output:
1

---

- sum()

Adds all values.
print(sum(t))

### Output
15

---

### 6. Tuple Methods

Tuples have only two methods.

- count()

Counts occurrences of a value.

t = (1,2,3,2,2)
print(t.count(2))

### Output
3

---

- index()

Returns first position of an element.

t = (1,2,3)
print(t.index(3))

### Output:
2

---

### 7. Packing and Unpacking

- Packing

Creating a tuple without brackets.

t = 1,2,3

---

- Unpacking

Assigning tuple values to variables.

a,b,c = t
print(a,b,c)

### Output:
1 2 3

---

### 8. Nested Tuples

A tuple can contain another tuple.

t = (1,(2,3),4)
print(t[1][0])

### Output:
2

---

### 9. Immutability of Tuple

Tuple elements cannot be changed.

t = (1,2,3)
t[0] = 10

### Output:

Error
But mutable objects inside tuples can change:

---
t = (1,[2,3])
t[1][0] = 99
print(t)

### Output:
(1,[99,3])

---

### 10. Converting Tuples

- Tuple → List

t = (1,2,3)
lst = list(t)

### Output:
[1,2,3]

---

- List → Tuple

t2 = tuple(lst)

### Output:
(1,2,3)

---

## Summary

### List:

- Mutable collection
- Uses square brackets [ ]
- Can add, remove, update elements
- More flexible

### Tuple:

- Immutable collection
- Uses parentheses ( )
- Cannot modify elements
- Faster and safer for fixed data

### Use List when data needs changes.
### Use Tuple when data should remain constant.
