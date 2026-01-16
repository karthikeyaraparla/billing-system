# Billing System – Git & Linux Commands

mkdir billing-system
cd billing-system
mkdir src config logs
touch README.md
touch src/app.py

git init
git add .
git commit -m "Initial project structure for billing system"

git branch -M main
git remote add origin https://github.com/karthikeyaraparla/billing-system.git
git push -u origin main

git checkout -b feature/add-billing-logic
git add src/app.py
git commit -m "Added basic billing calculation logic"
git push origin feature/add-billing-logic

git checkout main
git add src/app.py
git commit -m "Updated billing logic with discount"
git push origin main

git merge feature/add-billing-logic

git add src/app.py
git commit -m "Resolved merge conflict"
git push origin main
