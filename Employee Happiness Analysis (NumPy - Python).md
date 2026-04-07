# 📊 Employee Happiness Analysis (NumPy - Python)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![NumPy](https://img.shields.io/badge/Library-NumPy-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

This project analyzes **employee happiness and experience** using NumPy arrays.

The goal is to help HR:
- 📈 Understand employee satisfaction
- 🏢 Analyze department-wise trends
- ⏳ Evaluate experience vs happiness

---

## 🧩 Dataset Description

### 👨‍💼 Employee Details
Contains:
- Employee ID
- Department
- Years of Experience

```python
import numpy as np

employee_details = np.array([
    [101, 'Sales', 3],
    [102, 'HR', 5],
    [103, 'IT', 2],
    [104, 'Sales', 8],
    [105, 'IT', 6]
])
```

---

### 😊 Survey Results
Contains:
- Employee ID
- Happiness Score (1–10)

```python
survey_results = np.array([
    [101, 7],
    [102, 6],
    [103, 8],
    [104, 5],
    [105, 9]
])
```

---

## ⚙️ Tasks Performed

### 🔹 Task 1: Extract Columns

```python
employee_ids = employee_details[:, 0]
departments = employee_details[:, 1]
years = employee_details[:, 2]
```

---

### 🔹 Task 2: Match Employee ID with Happiness Score

```python
happiness_scores = survey_results[:, 1]
```

---

### 🔹 Task 3: Average Happiness Score

```python
avg_happiness = np.mean(happiness_scores)
print("Average Happiness:", avg_happiness)
```

---

### 🔹 Task 4: Department-wise Analysis

```python
sales_scores = []
it_scores = []
hr_scores = []

for i in range(len(employee_details)):
    dept = employee_details[i][1]
    score = survey_results[i][1]

    if dept == "Sales":
        sales_scores.append(score)
    elif dept == "IT":
        it_scores.append(score)
    elif dept == "HR":
        hr_scores.append(score)

print("Sales Avg:", np.mean(sales_scores))
print("IT Avg:", np.mean(it_scores))
print("HR Avg:", np.mean(hr_scores))
```

---

### 🔹 Task 5: High Experience Employees (>=5 years)

```python
for i in range(len(employee_details)):
    if int(employee_details[i][2]) >= 5:
        print(employee_details[i][0], "has high experience")
```

---

## 📊 Sample Output

```
Average Happiness: 7.0
Sales Avg: 6.0
IT Avg: 8.5
HR Avg: 6.0
102 has high experience
104 has high experience
105 has high experience
```

---

## 🧠 Key Concepts Learned

- 📦 NumPy Arrays
- 🔍 Indexing & Slicing
- 📊 Mean Calculation
- 🔄 Looping through arrays
- 📈 Basic Data Analysis

---

## 📁 Project Structure

```
employee-happiness-analysis/
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

- 🔹 Use Pandas for advanced analysis
- 🔹 Add data visualization (Matplotlib / Seaborn)
- 🔹 Create dashboard (Power BI / Streamlit)
- 🔹 Handle larger datasets

---

## 📈 Resume Value

> Analyzed employee satisfaction data using NumPy by performing array operations, statistical analysis, and department-wise insights to support HR decision-making.

---

## ⭐ If you like this project

Give it a ⭐ and keep learning 🚀
