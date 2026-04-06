# 📚 Library Management System (OOP - Python)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Concept](https://img.shields.io/badge/Concept-OOP-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

This project simulates a **Library Management System** where items such as books and journals can be borrowed and returned.

The system handles:
- 📖 Borrowing items
- 🔄 Returning items
- ⚠️ Exception handling for invalid operations
- 🧱 Object-Oriented Programming concepts

---

## 🧠 Concepts Used

- 🧱 Classes & Objects
- 🔁 Inheritance
- ⚙️ Method Overriding
- ❗ Exception Handling
- 📦 Encapsulation

---

## 🧩 Problem Statement

Design a system to manage library items with the following features:

- Track item availability
- Prevent borrowing already borrowed items
- Prevent returning items that are not borrowed
- Manage different item types (Books & Journals)

---

## ⚙️ Implementation

### 🔹 Base Class: LibraryItem

```python
class LibraryItem:
    def __init__(self, title, borrowed):
        self.title = title
        self.borrowed = borrowed

    def borrow_item(self):
        if self.borrowed:
            raise Exception(f"The item '{self.title}' is already borrowed.")
        self.borrowed = True
        return f"The item '{self.title}' is now borrowed."

    def return_item(self):
        if not self.borrowed:
            raise Exception(f"The item '{self.title}' is not borrowed.")
        self.borrowed = False
        return f"The item '{self.title}' has been returned."
```

---

### 🔹 Derived Class: Book

```python
class Book(LibraryItem):
    def __init__(self, title, author):
        super().__init__(title, False)
        self.author = author

    def details(self):
        return f"'{self.title}' by {self.author}"
```

---

### 🔹 Derived Class: Journal

```python
class Journal(LibraryItem):
    def __init__(self, title, issue_no):
        super().__init__(title, False)
        self.issue_no = issue_no

    def info(self):
        return f"{self.title} (Issue {self.issue_no})"
```

---

## 🧪 Example Usage

### 📖 Borrowing Example

```python
book = Book("The Magic of Thinking Big", "David Schwartz")

try:
    print(book.borrow_item())
    print(book.borrow_item())  # will raise exception
except Exception as e:
    print("Exception:", e)
```

### Output
```
The item 'The Magic of Thinking Big' is now borrowed.
Exception: The item 'The Magic of Thinking Big' is already borrowed.
```

---

### 🔄 Return Example

```python
journal = Journal("Nature", 123)

try:
    print(journal.return_item())  # not borrowed yet
except Exception as e:
    print("Exception:", e)
```

### Output
```
Exception: The item 'Nature' is not borrowed.
```

---

## 📁 Project Structure

```
library-management-system/
│── main.py
│── README.md
```

---

## 💡 Key Learnings

- ✔️ Designed reusable classes using OOP
- ✔️ Implemented inheritance for code reuse
- ✔️ Handled real-world edge cases using exceptions
- ✔️ Built a structured and scalable system

---

## 🚀 Future Improvements

- 🔹 Add user input system (CLI)
- 🔹 Store data in a file/database
- 🔹 Add due date & fine calculation
- 🔹 Build GUI using Tkinter or Web App using Flask

---

## 📈 Resume Value

> Developed a Library Management System using Python OOP principles with exception handling to manage borrowing and returning of items efficiently.

---

## ⭐ If you like this project

Give it a ⭐ and keep building amazing projects!

---
