# 📊 Employee Happiness Analysis (NumPy - Python)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![NumPy](https://img.shields.io/badge/Library-NumPy-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

This project analyzes employee happiness and experience using NumPy arrays.

It helps HR:
- 📈 Understand employee satisfaction  
- 🏢 Analyze department trends  
- ⏳ Evaluate experience vs happiness  

---

## 🧩 Problem Statement

At a software company, the HR team wants to understand how happy employees are with company policies and how long they've been with the company.

Two datasets are provided:

### 👨‍💼 Employee Details
- Employee ID  
- Department  
- Years of Experience  

### 😊 Survey Results
- Employee ID  
- Happiness Score (1–10)  

---

## 📂 Dataset

```python
import numpy as np

employee_details = np.array([
    [101, 'Sales', 3],  
    [102, 'HR', 5],    
    [103, 'IT', 2],        
    [104, 'Sales', 8],    
    [105, 'IT', 6],      
    [106, 'HR', 4],           
    [107, 'IT', 7],    
    [108, 'Sales', 1], 
    [109, 'HR', 3]          
])

survey_results = np.array([
    [101, 8],
    [102, 10],
    [103, 9],
    [104, 6],
    [105, 7],
    [106, 8],
    [107, 9],
    [108, 5],
    [109, 7]
])
```

---

# 🧩 Tasks & Solutions

---

## 🔹 Task 1: Merge Arrays

### Action
Combine both arrays using `np.hstack`.

```python
merged = np.hstack((employee_details, survey_results))
```

---

## 🔹 Task 2: Print Happiness Scores

### Action
Extract and print all happiness scores.

```python
hs = merged[:, 4]
print(hs)
```

---

## 🔹 Task 3: Sort Scores

### Action
Sort happiness scores in ascending order.

```python
hsa = hs.astype(float)
print(np.sort(hsa))
```

---

## 🔹 Task 4: Employee Details

### Action
Print Employee ID and Department.

```python
print(merged[:, 0:2])
```

---

## 🔹 Task 5: Employee ID with Happiness Score

### Action
Display Employee ID with Happiness Score.

```python
print(merged[:, 0:5:4])
```

---

## 🔹 Task 6: Convert Scores to Float

### Action
Convert scores to float.

```python
hsa = hs.astype(float)
```

---

## 🔹 Task 7: Average Happiness Score

### Action
Calculate average score.

```python
print(np.mean(hsa))
```

---

## 🔹 Task 8: Unique Departments

### Action
Find unique departments.

```python
dept = merged[:, 1]
print(np.unique(dept))
```

---

## 🔹 Task 9: HR Department Average Happiness

### Action
Filter HR department and calculate average score.

```python
hr = merged[merged[:, 1] == 'HR']
hr_scores = hr[:, 4].astype(float)

print(round(np.mean(hr_scores), 1))
```

---

## 📊 Sample Output

```
Sorted Scores: [5. 6. 7. 7. 8. 8. 9. 9. 10.]
Average Happiness: 7.66
Unique Departments: ['HR' 'IT' 'Sales']
HR Average Happiness: 7.3
```

---

## 🧠 Key Learnings

- 📦 NumPy array operations  
- 🔍 Indexing & slicing  
- 🔄 Data merging using `hstack`  
- 📊 Statistical analysis (mean, sort)  
- 🧠 Filtering data using conditions  

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

- Use Pandas for advanced analytics  
- Add visualizations (Matplotlib / Seaborn)  
- Build dashboard using Streamlit  
- Work with real-world datasets  

---

## 📈 Resume Value

> Performed employee happiness analysis using NumPy by applying array operations, sorting, filtering, and statistical techniques to derive insights for HR decision-making.

---

## ⭐ If you like this project

Give it a ⭐ and keep building 🚀
