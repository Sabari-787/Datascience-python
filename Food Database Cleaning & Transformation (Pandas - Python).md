# 🍽️ Food Database Cleaning & Transformation (Pandas - Python)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Library-Pandas-yellow)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

This project focuses on **data cleaning and transformation** of a food database using Pandas.

The goal is to:
- 🧹 Clean inconsistent data
- 🔄 Replace values using `.replace()`
- 🔢 Convert categorical data into numerical format

---

## 🧩 Problem Statement

A hotel owner maintains a dataset (`food_db.csv`) containing:

- food_id  
- name  
- discount  
- price  
- rating  

He wants to:
1. Update discount values to attract customers  
2. Convert rating categories into numerical values for analysis  

---

## 📂 Dataset

```python
import pandas as pd

df = pd.read_csv('food_db.csv')
```

---

# 🧩 Tasks & Solutions

---

## 🔹 Task 1: Load Dataset

### Action
- Read CSV file  
- Check shape  
- Display data  

```python
df = pd.read_csv('food_db.csv')

print(df.shape)
print(df.head())
```

---

## 🔹 Task 2: Replace Discount Values

### Action
Replace:
- `5%` → `13%`
- `10%` → `13%`

```python
new_df = df.replace(['10%', '5%'], '13%')

print(new_df)
```

---

## 🔹 Task 3: Convert Rating to Numeric

### Action
Convert categorical ratings:

- Excellent → 4  
- Very Good → 3  
- Good → 2  
- Average → 1  

```python
new_df = new_df.replace({
    'Excellent': 4,
    'Very Good': 3,
    'Good': 2,
    'Average': 1
})

print(new_df)
```

---

## 📊 Sample Output

```
Updated Discounts:
10% and 5% → 13%

Updated Ratings:
Excellent → 4
Very Good → 3
Good → 2
Average → 1
```

---

## 🧠 Key Learnings

- 🔄 Data cleaning using `.replace()`
- 🧹 Handling categorical data
- 🔢 Encoding categories into numbers
- 📊 Preparing data for analysis

---

## 📁 Project Structure

```
food-data-cleaning/
│── food_db.csv
│── main.py
│── README.md
```

---

## 🚀 How to Run

```bash
python main.py
```

---

## 💡 Future Improvements

- Convert price column to numeric  
- Perform statistical analysis  
- Add visualization (charts)  
- Build dashboard using Streamlit  

---

## 📈 Resume Value

> Cleaned and transformed food dataset using Pandas by replacing inconsistent values and encoding categorical data to prepare it for analysis.

---

## ⭐ If you like this project

Give it a ⭐ and keep building 🚀
