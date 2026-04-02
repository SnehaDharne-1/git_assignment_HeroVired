🧮 Q1: CalculatorPlus Application
<br>
📌 Objective
<br>
Enhance a Python calculator application by:
<br>
Adding square root functionality
<br>
Handling division by zero bug
<br>
Following proper Git workflow
<br>
🔀 Branching Strategy
<br>
main → Production-ready code
dev → Development branch
feature/sqrt → Square root feature
bugfix/divide-error (optional internal step)
⚙️ Steps Performed
<br>
1. Repository Setup
<br>
git init
<br>
git remote add origin <repo-link>
<br>
git branch -M main
<br>
git push -u origin main
<br>
3. Create and Work on dev Branch
   <br>
git checkout -b dev
Added base Calculator code
<br>
5. Implement Square Root Feature
<br>
Uncommented and implemented:
<br>
def square_root(self, x):
    return math.sqrt(x)
   <br>
4. Merge dev → main (Version 1 Release)
   <br>
git checkout main
git merge dev
git tag v1.0
git push origin v1.0
<br>
5. Add Collaborator
   <br>
Added classmate as collaborator for code review
<br>
6. Create Feature Branch
<br>
git checkout -b feature/sqrt
<br>
7. Bug Fix (Divide by Zero)
   <br>

Updated function:

def divide(self, a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b
    <br>
8. Keep Feature Branch Updated 
<br>
git checkout dev
git pull origin dev
git checkout feature/sqrt
git merge dev
<br>
9. Pull Request Workflow
<br>
Created PR: feature/sqrt → main
Requested code review
Applied feedback
Merged after approval
<br>
10. Final Merge & Version 2 Release
<br>
git checkout dev
git merge feature/sqrt
git checkout main
git merge dev
git tag v2.0
git push origin v2.0
<br>
📦 Q2: Git LFS (Large File Storage)
📌 Objective

Handle large binary files (>200MB) using Git LFS

⚙️ Steps Performed
<br>
1. Install Git LFS
git lfs install
<br>
2. Create lfs Branch
git checkout -b lfs
<br>
3. Track Large Files
git lfs track "*.zip"
<br>
4. Add & Commit File
git add .gitattributes
git add large_file.zip
git commit -m "Added large file using Git LFS"
git push origin lfs
<br>
5. Verification
Cloned repo on another system:
git clone <repo-link>
Verified large file downloaded correctly via LFS
<br>
📐 Q3: Geometry Calculator with Git Stash
📌 Objective

Develop features using Git stash to manage incomplete work.

🔀 Branches Used
geometry-calculator
feature/circle-area
feature/rectangle-area
⚙️ Workflow Steps
<br>
1. Create Base Branch
git checkout -b geometry-calculator
<br>
2. Circle Area Feature
git checkout -b feature/circle-area
Worked on circle area
Stashed changes:
git stash
git status
<br>
3. Rectangle Area Feature
git checkout -b feature/rectangle-area
Worked on rectangle area
Stashed changes:
git stash
<br>
4. Resume Circle Feature
git checkout feature/circle-area
git stash pop

Completed:

radius = 5
print(f"The area of the circle = {calculator.calculate_circle_area(radius)}")
<br>
5. Commit & Push
git add .
git commit -m "Completed circle area feature"
git push origin feature/circle-area
<br>
6. Resume Rectangle Feature
git checkout feature/rectangle-area
git stash pop

Completed:

length = 10
width = 6
print(f"Rectangle area = {calculator.calculate_rectangle_area(length, width)}")
<br>
7. Commit & Push
git add .
git commit -m "Completed rectangle area feature"
git push origin feature/rectangle-area
<br>
8. Pull Requests
Created PRs to dev branch
Requested reviews
Merged after approval
