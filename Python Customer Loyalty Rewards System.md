# 🎯 Customer Loyalty Rewards System (Python)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Level](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-orange)

---

## 📌 Project Overview

This project simulates a **Customer Loyalty Rewards Program** where customers are assigned reward levels based on their total purchase amount.

It demonstrates core Python concepts including:
- 📂 File Handling
- 🔁 Loops
- 🔤 Dictionaries
- 📦 Tuples
- ⚙️ Functions
- 🔀 Conditional Logic

---

## 🧩 Problem Statement

Given a file containing customer purchase data:

```
Srinivas,120
John,250
Maria,150
Smith,510
Anjali,45
```

We need to:
1. Read the file
2. Store data in a dictionary
3. Assign reward levels
4. Create a final summary

---

## 🏆 Reward Criteria

| Purchase Amount | Reward Level |
|---------------|-------------|
| 100 – 199     | Bronze 🟤   |
| 200 – 499     | Silver ⚪   |
| 500+          | Gold 🟡     |
| < 100         | None ❌     |

---

## ⚙️ Implementation

### 🔹 Step 1: Read File & Create Dictionary

```python
customers_dict = {}

with open("customers.txt", "r") as f:
    for line in f:
        name, amount = line.strip().split(",")
        customers_dict[name] = int(amount)
```

---

### 🔹 Step 2: Reward Calculation Function

```python
def calculate_rewards(total):
    if total >= 500:
        return "Gold"
    elif total >= 200:
        return "Silver"
    elif total >= 100:
        return "Bronze"
    else:
        return "None"
```

---

### 🔹 Step 3: Create Customer Summary

```python
customer_summary = {}

for name, total in customers_dict.items():
    reward = calculate_rewards(total)
    customer_summary[name] = (total, reward)
```

---

### 🔹 Step 4: Final Function (Complete Solution)

```python
def process_customer_data(filename):
    customers_dict = {}

    # Read file
    with open(filename, "r") as f:
        for line in f:
            name, amount = line.strip().split(",")
            customers_dict[name] = int(amount)

    # Generate summary
    customer_summary = {}
    for name, total in customers_dict.items():
        reward = calculate_rewards(total)
        customer_summary[name] = (total, reward)

    return customer_summary
```

---

## 📊 Example Output

```python
{
 'Srinivas': (120, 'Bronze'),
 'John': (250, 'Silver'),
 'Maria': (150, 'Bronze'),
 'Smith': (510, 'Gold'),
 'Anjali': (45, 'None')
}
```

---

## 🧠 Key Concepts Learned

- 📂 Reading files using `with open()`
- 🔄 Iterating through file line-by-line
- 🧠 Using dictionaries for data storage
- 📦 Using tuples for structured output
- ⚙️ Writing reusable functions
- 🔀 Applying conditional logic

---

## 📁 Project Structure

```
customer-loyalty-system/
│── customers.txt
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

- 🔹 Add user input for dynamic data
- 🔹 Store output in a new file
- 🔹 Convert into a web app (Flask)
- 🔹 Visualize rewards using charts

---

## 📈 Resume Value

> Built a customer loyalty reward system using Python by implementing file handling, functions, dictionaries, and conditional logic to process and categorize real-world data.

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and keep building!

---
