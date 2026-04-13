# 📘 Git Assignment – Hero Vired

## 📌 Repository Name
git_assignment_HeroVired

This repository demonstrates Git and GitHub workflows including branching strategies, pull requests, Git LFS, and Git stash.
---

## 📖 Description

This repository contains the complete solution for the Hero Vired Git assignment. It demonstrates:
- Branching strategy (main, dev, feature branches)
- Feature implementation (square root)
- Bug fixing workflow
- Version releases (v1.0 & v2.0)
- Git LFS usage
- Git stash workflow

---

# 🧮 Q1: CalculatorPlus Application

## 🚀 Objective
Step 1 – Repository Setup
A private GitHub repository named git_assignment_HeroVired was created and cloned locally.
```
git clone <repository-url>
cd git_assignment_HeroVired
```
---

## 🧾 Calculator Code

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
        if b == 0:
            raise ValueError("Cannot divide by zero.")
        return a / b

    def square_root(self, x):
        return math.sqrt(x)

if __name__ == "__main__":
    calculator = Calculator()

    num1 = 16
    num2 = 4

    print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
    print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
    print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
    print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")

    num3 = 25
    print(f"The square root of {num3} = {calculator.square_root(num3)}")

```
    
1️⃣ Create Repository
```python

git init
git remote add origin <your-repo-link>
git branch -M main
git push -u origin main

```
2️⃣ Create DEV Branch and Add Code

```
git checkout -b dev
git add .
git commit -m "Added calculator base code"
git push origin dev
```

3️⃣ Merge DEV → MAIN (Version 1 Release)
```
git checkout main
git merge dev
git tag v1.0
git push origin main --tags

```

4️⃣ Create Feature Branch (feature-sqrt)

```
git checkout -b feature-sqrt

```

5️⃣ Add Square Root Feature
Implemented square_root() function using math.sqrt()

6️⃣ Fix Bug in Divide Function

```
def divide(self, a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b
```

7️⃣ Merge Feature → DEV

```
git checkout dev
git merge feature-sqrt
git push origin dev

```

8️⃣ Merge DEV → MAIN (Version 2 Release)

```
git checkout main
git merge dev
git tag v2.0
git push origin main --tags

```
9️⃣ Collaboration
Added a classmate as collaborator
Performed code review on peer repository

### 📦 Q2: Git LFS (Large File Storage)
🚀 Steps

```
git lfs install
git checkout -b lfs
git lfs track "*.zip"
git add .gitattributes
git add large_file.zip
git commit -m "Added large file using Git LFS"
git push origin lfs

```
### 📦 Q3 – Geometry Calculator Using Git Stash
Create Branch

```
git checkout -b geometry-calculator

```
Created file:

geometry.py

### Feature Branch – Circle Area
```
git checkout -b feature/circle-area
```
Circle area calculation was implemented:
```
Area = π × radius²
```
Before committing, incomplete changes were stored using:
```
git stash
```
### Feature Branch – Rectangle Area

```
git checkout -b feature/rectangle-area
Area = length × width    
git stash
```

### Restore Stashed Work
```
git stash pop

```

### Pull Requests
```
feature/circle-area → dev
feature/rectangle-area → dev
```

After review, both pull requests were merged.

Finally, the dev branch was merged into main.

```
git checkout main
git merge dev
git push origin main

```
```
main
dev
feature/sqrt
feature/circle-area
feature/rectangle-area
geometry-calculator
lfs
```

### Version Releases

```
v1.0 – Initial release of CalculatorPlus
v2.0 – Added square root functionality and bug fix
```

### Git Log Visualization

```
git log --graph --oneline --decorate --all

```
