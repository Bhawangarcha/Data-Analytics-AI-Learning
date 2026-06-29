#Python Dictionary 

###What is a Dictionary?
A dictionary is a built-in data structure in Python that is used to store a collection of data in the form of key-value pairs.
Each item in a dictionary has two parts:
- Key → A unique identifier
- Value → The data associated with that key
### Example:
student = {
    "name": "Alice",
    "age": 25,
    "course": "Python"
}

- Here:

"name" is a key
"Alice" is its value

- Dictionaries are useful when we need to store data that can be searched using a meaningful name instead of an index.

---

### Features of Dictionary

### 1. Mutable

A dictionary can be modified after creation.

We can:

- Add new elements
- Update existing values
- Delete elements

### Example:
student = {"name":"John"}
student["name"] = "David"
print(student)

### Output:

{'name': 'David'}

---

### 2. Stored as Key-Value Pairs
Unlike lists and tuples which store values using positions, dictionaries store values using keys.

### List example:

numbers = [10,20,30]
print(numbers[0])
Dictionary example:
student = {"marks":90}
print(student["marks"])

---

### 3. Keys Must Be Unique

Every key in a dictionary should be different.

### Example:

d = {
"name":"John",
"name":"Alex"
}

print(d)

### Output:

{'name':'Alex'}

The latest value replaces the previous value.

---

### 4. Keys Must Be Immutable
Keys cannot be changed.

### Valid keys:

- "age"
- 10
- (1,2)

### Invalid key:

[1,2,3]

because lists are mutable.

---

### 5. Values Can Be Any Data Type

Values can store:
- Integer
- Float
- String
- List
- Tuple
- Dictionary
- Objects

### Example:

data = {
"name":"Tom",
"marks":[90,80,85],
"active":True
}

---

### Creating a Dictionary

- Using Curly Braces {}

student = {
"name":"Tom",
"age":20
}

---

- Using dict()

student = dict(name="Tom", age=20)
print(student)

### Output:

{'name':'Tom','age':20}

---

### Empty Dictionary

data = {}

Used when we want to add data later.

### Example:

data = {}
data["name"] = "Ali"
data["age"] = 21
print(data)

---

### Accessing Dictionary Elements

- Using Key

student = {
"name":"John",
"age":30
}

print(student["name"])

### Output:

John

If the key does not exist, it gives an error.

---

- Using get() Method

get() is a safer way to access values.

print(student.get("age"))

### Output:

30

If key is missing:

print(student.get("city"))

### Output:

None

---

### Adding Elements

New key-value pairs can be added by using a new key.

### Example:

student = {
"name":"John"
}

student["city"] = "Delhi"

print(student)

### Output:

{'name':'John','city':'Delhi'}

---

### Updating Dictionary

Existing values can be changed.

student = {
"name":"John",
"age":20
}

student["age"] = 25
print(student)

### Output:

{'name':'John','age':25}

---

### Removing Elements

pop()

Removes a specific key.

student.pop("age")

---

### del Keyword

Deletes an item.

del student["name"]

---

### clear()

Deletes all items.

student.clear()

###Output:

{}


---

### Dictionary Methods

keys()

Returns all keys.

student.keys()

Example:

student = {"name":"Tom","age":20}
for x in student.keys():
    print(x)

### Output:

name
age


---

values()

Returns all values.

for x in student.values():
    print(x)

Output:

Tom
20


---

items()

Returns key-value pairs.

for key,value in student.items():
    print(key,value)

Output:

name Tom
age 20


---

update()

Used to combine dictionaries.

Example:

a = {
"name":"Tom"
}

b = {
"age":20
}

a.update(b)

print(a)

Output:

{'name':'Tom','age':20}


---

copy()

Creates a copy of dictionary.

new = student.copy()

Changes in the copy do not affect original dictionary.


---

Dictionary Looping

Loop through Keys

student = {
"name":"Tom",
"age":20
}

for x in student:
    print(x)


---

Loop through Values

for x in student.values():
    print(x)


---

Loop through Key and Value

for k,v in student.items():
    print(k,v)


---

Nested Dictionary

A dictionary inside another dictionary is called a nested dictionary.

Example:

students = {

"student1":{

"name":"Tom",
"marks":90

},

"student2":{

"name":"Alex",
"marks":85

}

}

Access:

print(students["student1"]["marks"])

Output:

90


---

Difference Between Dictionary and List

Dictionary	List

Stores key-value pairs	Stores values only
Uses keys for access	Uses index for access
Keys must be unique	Index can repeat values
Mutable	Mutable
Faster searching by key	Searching requires index



---

Real-Life Examples of Dictionary

Student Record

student = {
"name":"Rahul",
"roll_no":101,
"marks":95
}

Employee Data

employee = {
"id":1,
"name":"John",
"salary":50000
}

Product Details

product = {
"name":"Laptop",
"price":50000,
"brand":"Dell"
}


---

Advantages of Dictionary

Fast data retrieval

Easy to update data

Stores related information together

Flexible structure

Supports nested data



---

Summary

A Python dictionary is a mutable, unordered (logically ordered from Python 3.7+) collection of key-value pairs used to store and manage data efficiently. It provides methods like keys(), values(), items(), get(), and update() to work with data easily.
