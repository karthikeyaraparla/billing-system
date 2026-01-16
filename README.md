Billing-system

 1. Set up the Project Structure using Linux Commands

mkdir billing-system

Creates a new directory called `billing-system` for the project.


cd billing-system


Moves inside the project directory.


mkdir src config logs


Creates folders for source code, configuration files, and logs.


touch README.md


Creates a README file to document the project.


touch src/app.py


Creates the main backend application file.



## 2. Initialize Git

git init

Initializes a new Git repository to start version control.

git add .

Adds all project files to the staging area.


git commit -m "Initial project structure for billing system"

Commits the project structure with a meaningful message.


## 3. Push the Project to GitHub

git branch -M main

Renames the default branch to `main`.

git remote add origin https://github.com/username/billing-system.git

Connects the local project to a remote GitHub repository.

git push -u origin main


Pushes the code to GitHub and sets `main` as the default branch.

## 4. Create a Feature Branch

git checkout -b feature/add-billing-logic

Creates and switches to a new feature branch for billing logic development.

def calculate_bill(amount, tax):
    return amount + (amount * tax)


Adds basic billing calculation logic.

git add src/app.py


Stages the updated billing logic file.


git commit -m "Added basic billing calculation logic"


Commits the feature change.


git push origin feature/add-billing-logic


Pushes the feature branch to GitHub.


## 5. Simulate a Team Change

git checkout main

Switches back to the main branch (simulating another developer’s work).

def calculate_bill(amount, tax, discount):
    return amount + (amount * tax) - discount

Updates the same function with discount logic.

git add src/app.py

Stages the modified file.

git commit -m "Updated billing logic with discount"

Commits the team member’s change.

git push origin main

Pushes the changes to the main branch.


## 6. Merge the Code


git merge feature/add-billing-logic


Attempts to merge the feature branch into main.

This causes a merge conflict because the same file was changed in both branches.


## 7. Handle a Merge Conflict


<<<<<<< HEAD
def calculate_bill(amount, tax, discount):
    return amount + (amount * tax) - discount
=======
def calculate_bill(amount, tax):
    return amount + (amount * tax)
>>>>>>> feature/add-billing-logic

git add src/app.py
Marks the conflict as resolved.
git commit -m "Resolved merge conflict in billing logic"
Commits the resolved code.
git push origin main


Pushes the final merged code to GitHub.

