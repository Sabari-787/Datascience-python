# 📊 Python Data Analysis Mini Projects (Comprehensions & Sets)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Concepts](https://img.shields.io/badge/Concepts-Comprehensions%20%7C%20Sets-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

This project consists of **multiple real-world mini tasks** solved using Python.

It demonstrates:
- 🧠 Set operations
- ⚡ List, Set & Dictionary Comprehensions
- 📊 Data filtering techniques
- 🔍 Pattern extraction from text

---

# 🧩 Tasks & Solutions

---

## 🔹 Task 1: Inventory Analysis

### 🎯 Objective
Find **unique product categories**.

### 💻 Code

```python
products = [
    {"product_name": "Laptop", "category": "Electronics", "price": 1200},
    {"product_name": "Jeans", "category": "Apparel", "price": 40},
    {"product_name": "Coffee Maker", "category": "Home Appliances", "price": 80},
    {"product_name": "Smartphone", "category": "Electronics", "price": 999},
    {"product_name": "Jacket", "category": "Apparel", "price": 60},
    {"product_name": "Blender", "category": "Home Appliances", "price": 150},
    {"product_name": "Book", "category": "Literature", "price": 15}
]

unique_categories = {p['category'] for p in products}
print(unique_categories)
```

### 📊 Output
```
{'Apparel', 'Electronics', 'Home Appliances', 'Literature'}
```

---

## 🔹 Task 2: Audience Analysis

### 🎯 Objective
Find:
- Unique attendees
- Common attendees

### 💻 Code

```python
a = {"Alice", "Bob", "Charlie", "Diana"}
b = {"Bob", "Diana", "Eve", "Frank"}
c = {"Alice", "George", "Elle", "Frank", "Bob"}

print("Concert A Only:", a - b - c)
print("Concert B Only:", b - a - c)
print("Concert C Only:", c - a - b)
print("Common Attendees:", a & b & c)
```

### 📊 Output
```
Concert A Only: {'Charlie'}
Concert B Only: {'Eve'}
Concert C Only: {'Elle', 'George'}
Common Attendees: {'Bob'}
```

---

## 🔹 Task 3: Temperature Filtering

### 🎯 Objective
Find temperatures > 70°F

### 💻 Code

```python
daily_temperatures = [68, 71, 74, 69, 70, 71, 68, 73, 72, 71, 70, 74, 72, 68]

high_temp = [t for t in daily_temperatures if t > 70]
print(high_temp)
```

### 📊 Output
```
[71, 74, 71, 73, 72, 71, 74, 72]
```

---

## 🔹 Task 4: Unique Temperatures

### 🎯 Objective
Get unique values

### 💻 Code

```python
unique_temp = {t for t in daily_temperatures}
print(unique_temp)
```

### 📊 Output
```
{68, 69, 70, 71, 72, 73, 74}
```

---

## 🔹 Task 5: Temperature Frequency

### 🎯 Objective
Count occurrences

### 💻 Code

```python
temp_freq = {t: daily_temperatures.count(t) for t in daily_temperatures}
print(temp_freq)
```

### 📊 Output
```
{68: 3, 71: 3, 74: 2, 69: 1, 70: 2, 73: 1, 72: 2}
```

---

## 🔹 Task 6: Social Media Analysis

### 🎯 Objective
Filter posts with >100 likes

### 💻 Code

```python
posts = [
    {"content": "Loving the sunny weather today! #sunny #happy", "likes": 120},
    {"content": "Nothing beats a beach day. #beachday #sunny", "likes": 350},
    {"content": "A rainy day at home. #rainy #lazyday", "likes": 75},
    {"content": "Best coffee in town. #coffeelove #morning", "likes": 180},
    {"content": "Can't wait for the weekend. #weekend #party", "likes": 90}
]

popular_posts = [p for p in posts if p['likes'] > 100]
print(popular_posts)
```

---

## 🔹 Task 7: Extract Hashtags

### 🎯 Objective
Get all hashtags

### 💻 Code

```python
hashtags = [
    word for p in popular_posts
    for word in p['content'].split()
    if word.startswith('#')
]

print(hashtags)
```

---

## 🔹 Task 8: Hashtag Frequency

### 🎯 Objective
Count hashtags

### 💻 Code

```python
hashtag_freq = {h: hashtags.count(h) for h in hashtags}
print(hashtag_freq)
```

### 📊 Output
```
{'#sunny': 2, '#happy': 1, '#beachday': 1, '#coffeelove': 1, '#morning': 1}
```

---

# 🧠 Key Learnings

- ⚡ List, Set, Dictionary Comprehensions  
- 🔍 Data filtering techniques  
- 📊 Frequency analysis  
- 🧠 Set operations (union, intersection, difference)  
- 📈 Real-world problem solving  

---

# 📁 Project Structure

```
python-mini-projects/
│── main.py
│── README.md
```

---

# 🚀 How to Run

```bash
python main.py
```

---

# 💡 Future Improvements

- 📊 Add visualization (Matplotlib)
- 🌐 Build dashboard (Streamlit)
- 🤖 Integrate ML models

---

# 📈 Resume Value

> Implemented Python-based data analysis tasks using comprehensions and set operations to solve real-world business scenarios including inventory analysis, audience insights, and social media analytics.

---

# ⭐ If you like this project

Give it a ⭐ and keep building 🚀
