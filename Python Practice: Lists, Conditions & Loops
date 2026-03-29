# 📘 Python Practice: Lists, Conditions & Loops

## 📌 Overview
This project demonstrates fundamental Python concepts using simple problem statements.

### Concepts Covered:
- Lists
- Indexing & Slicing
- List Methods (`append`, `insert`, `remove`)
- Loops (`for loop`)
- Conditional Statements (`if-elif-else`)
- `zip()` function

---

## 🧩 Task 1: Count Elements in a List

### Problem
Create a list of superheroes and count the number of elements.

### Solution
```python
avengers = ['Iron Man', 'Captain America', 'Black Widow', 'Hulk', 'Thor', 'Hawkeye']

print(len(avengers))
```

---

## 🧩 Task 2: Add Element to List

### Problem
Add a new superhero to the list.

### Solution
```python
avengers.append("Spiderman")
```

---

## 🧩 Task 3: Insert Element at Specific Position

### Problem
Move "Captain America" to the first position.

### Solution
```python
avengers.remove("Captain America")
avengers.insert(0, "Captain America")
```

---

## 🧩 Task 4: Reorder Elements

### Problem
Place "Black Widow" between Hulk and Thor.

### Solution
```python
avengers.remove("Black Widow")
avengers.insert(3, "Black Widow")

print(avengers)
```

---

## 🧩 Task 5: List Indexing & Slicing

### Problem
Access specific elements from a list of scores.

### Solution
```python
scores = [92, 85, 76, 58, 89, 91, 73, 84]

# First student
print(scores[0])

# Last student
print(scores[-1])

# First 3 students
print(scores[:3])

# Roll numbers 3, 4, 5
print(scores[2:5])
```

---

## 🧩 Task 6: Append New Data

### Problem
Add a new score to the list.

### Solution
```python
scores.append(83)

print(scores)
```

---

## 🧩 Task 7: Grade Classification System

### Problem
Classify scores into grades:

- A: 90–100  
- B: 80–89  
- C: 70–79  
- D: 60–69  
- F: Below 60  

### Solution
```python
scores = [92, 85, 76, 58, 89, 91, 73, 84, 83]

A, B, C, D, F = 0, 0, 0, 0, 0

for score in scores:
    if 90 <= score <= 100:
        A += 1
    elif 80 <= score < 90:
        B += 1
    elif 70 <= score < 80:
        C += 1
    elif 60 <= score < 70:
        D += 1
    else:
        F += 1

print("Grade Summary:")
print(f"A: {A} students")
print(f"B: {B} students")
print(f"C: {C} students")
print(f"D: {D} students")
print(f"F: {F} students")
```

### ⚠️ Common Mistake
```python
for i, score in enumerate(scores):
```

This is correct, but errors occur if `scores` becomes an integer accidentally.

---

## 🧩 Task 8: Inventory Management System

### Problem
Identify products that need restocking.

### Solution
```python
product_names = ["Apples", "Bananas", "Oranges", "Pears", "Grapes"]
stock_levels = [20, 50, 15, 5, 8]

minimum_stock = 10

reorder = []

for product, stock in zip(product_names, stock_levels):
    if stock < minimum_stock:
        reorder.append(product)

print("Items to reorder:", reorder)
```

---

## 🧠 Key Concepts Summary

### 🔹 List Methods
```python
append()
insert()
remove()
```

### 🔹 Indexing
```python
scores[0]
scores[-1]
```

### 🔹 Slicing
```python
scores[:3]
scores[2:5]
```

### 🔹 Loop
```python
for item in list:
```

### 🔹 Condition
```python
if condition:
elif condition:
else:
```

### 🔹 Zip Function
```python
zip(list1, list2)
```

---
