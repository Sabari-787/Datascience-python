# 🏠 Bengaluru House Price Analysis (Pandas - Python)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Library-Pandas-yellow)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

This project analyzes **house price data in Bengaluru** to help a user find suitable houses based on:

- 📍 Location  
- 💰 Budget  
- 🏠 House type  

It demonstrates practical usage of **Pandas for data analysis**.

---

## 🧩 Problem Statement

A person is searching for a house in Bengaluru and needs insights from a dataset containing:

- Area Type  
- Availability  
- Location  
- Size  
- Total Square Feet  
- Number of Bathrooms  
- Price  

Your task is to analyze this dataset and answer key questions.

---

## 📂 Dataset

```python
import pandas as pd

df = pd.read_csv("bengaluru_house_prices.csv")
```

---

# 🧩 Tasks & Solutions

---

## 🔹 Question 1: Basic Data Exploration

### Task
- Read CSV file  
- Print shape  
- Display top 5 rows  

### Solution
```python
df = pd.read_csv('bengaluru_house_prices.csv')

print(df.shape)
print(df.head(5))
```

---

## 🔹 Question 2: Unique Categories

### Task
Find unique values in:
- `area_type`
- `size`

### Solution
```python
print(df['area_type'].unique())
print(df['size'].unique())
```

---

## 🔹 Question 3: Filtering Data

### Task
Filter houses with:
- Size = **2 BHK**
- Area Type = **Super built-up Area**

### Solution
```python
df_fill = df[(df['size'] == '2 BHK') & 
             (df['area_type'] == 'Super built-up  Area')]

print(df_fill.head())
print("Count:", len(df_fill))
```

---

## 🔹 Question 4: Add New Column

### Task
Create a column:
- `price_category`
  - < 80 → Affordable  
  - >= 80 → High Cost  

### Solution
```python
df['price_Cat'] = df['price'].apply(
    lambda x: "Affordable" if x < 80 else "High Cost"
)

print(df.head())
```

---

## 🔹 Question 5: Above Average Price

### Task
Find houses where price is greater than average.

### Solution
```python
avg_price = df['price'].mean()

high_price_df = df[df['price'] > avg_price]

print(high_price_df.head())
```

---

## 📊 Sample Output Insights

- Average Price ≈ **82.07**
- Affordable vs High Cost classification added
- Filtered premium houses identified

---

## 🧠 Key Learnings

- 📊 Data loading using Pandas  
- 🔍 Filtering data using conditions  
- 🧮 Aggregation (`mean`)  
- 🏷️ Creating new columns  
- 📈 Data exploration  

---

## 📁 Project Structure

```
bengaluru-house-analysis/
│── bengaluru_house_prices.csv
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

- 🔹 Data cleaning (handle missing values)  
- 🔹 Feature engineering  
- 🔹 Visualization (Matplotlib / Seaborn)  
- 🔹 Build ML model for price prediction  

---

## 📈 Resume Value

> Analyzed real estate dataset using Pandas by performing data filtering, transformation, and statistical analysis to derive actionable insights.

---

## ⭐ If you like this project

Give it a ⭐ and keep building 🚀
