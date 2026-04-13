# 📘 Git Assignment – Question 1 (CalculatorPlus)

## 📌 Repository Name
`git_assignment_HeroVired`

---

## 📖 Description
This repository demonstrates the implementation of a simple Python application **CalculatorPlus** using proper Git workflow.

The assignment includes:
- Creating branches
- Adding features
- Merging code
- Releasing versions

---

## 🔀 Branch Workflow

- `main` → Production branch  
- `dev` → Development branch  
- `feature-sqrt` → Feature branch for square root  

---

## ⚙️ Steps Performed

### 1️⃣ Create Repository
- Created a GitHub repository named:
```
git_assignment_HeroVired
```

---

### 2️⃣ Create DEV Branch
```bash
git checkout -b dev
```

---

### 3️⃣ Add Calculator Code in DEV Branch

```python
import math

class Calculator:

    def add(self, a, b):
        return a + b

    def subtract(self, a, b):
        return a - b

    def multiply(self, a, b):
        return a * b

    def divide(self, a, b):
        return a / b

if __name__ == "__main__":
    calculator = Calculator()

    num1 = 16
    num2 = 4

    print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
    print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
    print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
    print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")
```

---

### 4️⃣ Merge DEV → MAIN & Release Version 1

```bash
git checkout main
git merge dev
git tag v1.0
git push origin v1.0
```

✅ Version 1 released with basic calculator features

---

### 5️⃣ Create Feature Branch (Square Root)

```bash
git checkout -b feature-sqrt
```

---

### 6️⃣ Add Square Root Feature

```python
def square_root(self, x):
    return math.sqrt(x)
```

Updated main execution:

```python
num3 = 25
print(f"The square root of {num3} = {calculator.square_root(num3)}")
```

---

### 7️⃣ Push Feature to DEV Branch

```bash
git checkout dev
git merge feature-sqrt
git push origin dev
```

---

### 8️⃣ Merge DEV → MAIN & Release Version 2

```bash
git checkout main
git merge dev
git tag v2.0
git push origin v2.0
```

✅ Version 2 released with square root feature

---

## 🚀 Final Outcome

- ✔️ Created repository and branches  
- ✔️ Implemented calculator functionality  
- ✔️ Added square root feature  
- ✔️ Followed proper Git workflow  
- ✔️ Released two versions (v1.0 & v2.0)  

---

## 📎 Submission

Repository link submitted via VLearn as per instructions.
