🧮 Q1: CalculatorPlus Application
📌 Objective

Enhance a Python calculator application by:

Adding square root functionality
Handling division by zero bug
Following proper Git workflow
🔀 Branching Strategy
main → Production-ready code
dev → Development branch
feature/sqrt → Square root feature
bugfix/divide-error (optional internal step)
⚙️ Steps Performed
1. Repository Setup
git init
git remote add origin <repo-link>
git branch -M main
git push -u origin main
2. Create and Work on dev Branch
git checkout -b dev
Added base Calculator code
3. Implement Square Root Feature

Uncommented and implemented:

def square_root(self, x):
    return math.sqrt(x)
4. Merge dev → main (Version 1 Release)
git checkout main
git merge dev
git tag v1.0
git push origin v1.0
5. Add Collaborator
Added classmate as collaborator for code review
6. Create Feature Branch
git checkout -b feature/sqrt
7. Bug Fix (Divide by Zero)

Updated function:

def divide(self, a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b
8. Keep Feature Branch Updated
git checkout dev
git pull origin dev
git checkout feature/sqrt
git merge dev
9. Pull Request Workflow
Created PR: feature/sqrt → main
Requested code review
Applied feedback
Merged after approval
10. Final Merge & Version 2 Release
git checkout dev
git merge feature/sqrt
git checkout main
git merge dev
git tag v2.0
git push origin v2.0
📦 Q2: Git LFS (Large File Storage)
📌 Objective

Handle large binary files (>200MB) using Git LFS

⚙️ Steps Performed
1. Install Git LFS
git lfs install
2. Create lfs Branch
git checkout -b lfs
3. Track Large Files
git lfs track "*.zip"
4. Add & Commit File
git add .gitattributes
git add large_file.zip
git commit -m "Added large file using Git LFS"
git push origin lfs
5. Verification
Cloned repo on another system:
git clone <repo-link>
Verified large file downloaded correctly via LFS
📐 Q3: Geometry Calculator with Git Stash
📌 Objective

Develop features using Git stash to manage incomplete work.

🔀 Branches Used
geometry-calculator
feature/circle-area
feature/rectangle-area
⚙️ Workflow Steps
1. Create Base Branch
git checkout -b geometry-calculator
2. Circle Area Feature
git checkout -b feature/circle-area
Worked on circle area
Stashed changes:
git stash
git status
3. Rectangle Area Feature
git checkout -b feature/rectangle-area
Worked on rectangle area
Stashed changes:
git stash
4. Resume Circle Feature
git checkout feature/circle-area
git stash pop

Completed:

radius = 5
print(f"The area of the circle = {calculator.calculate_circle_area(radius)}")
5. Commit & Push
git add .
git commit -m "Completed circle area feature"
git push origin feature/circle-area
6. Resume Rectangle Feature
git checkout feature/rectangle-area
git stash pop

Completed:

length = 10
width = 6
print(f"Rectangle area = {calculator.calculate_rectangle_area(length, width)}")
7. Commit & Push
git add .
git commit -m "Completed rectangle area feature"
git push origin feature/rectangle-area
8. Pull Requests
Created PRs to dev branch
Requested reviews
Merged after approval
