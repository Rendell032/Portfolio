# Git and GitHub Workflow Manual

## Project

Repository: `literacy-and-poverty-analysis`

GitHub URL: `https://github.com/Rendell032/literacy-and-poverty-analysis`

---

# Daily Workflow

## 1. Before starting work

Always pull the newest version first.

```bash
git pull
```

This gets the latest changes from GitHub.

---

## 2. Check project status

```bash
git status
```

Use this often. It tells you what changed.

---

## 3. After editing files

Stage your changes:

```bash
git add .
```

Or stage one file:

```bash
git add filename
```

Example:

```bash
git add .gitignore
```

---

## 4. Commit your changes

```bash
git commit -m "Short message describing the change"
```

Examples:

```bash
git commit -m "Update gitignore for virtual environments"
git commit -m "Add literacy dataset overview"
git commit -m "Complete initial literacy EDA"
```

---

## 5. Push to GitHub

```bash
git push
```

This uploads your local commits to GitHub.

---

# Full Workflow

Use this when you are done working:

```bash
git status
git add .
git commit -m "Describe what you changed"
git push
git status
```

---

# Switching Between Windows and Mac

## On the machine you are about to use

Always start with:

```bash
git pull
```

## When done working

Always finish with:

```bash
git add .
git commit -m "Describe what you changed"
git push
```

---

# Windows Setup

Go into the project folder:

```powershell
cd G:\literacy-and-poverty-analysis
```

Activate Windows virtual environment:

```powershell
.venv-windows\Scripts\Activate.ps1
```

If the venv does not exist:

```powershell
python -m venv .venv-windows
.venv-windows\Scripts\Activate.ps1
pip install -r requirements.txt
```

---

# Mac Setup

Go into the project folder:

```bash
cd path/to/literacy-and-poverty-analysis
```

Activate Mac virtual environment:

```bash
source .venv-mac/bin/activate
```

If the venv does not exist:

```bash
python3 -m venv .venv-mac
source .venv-mac/bin/activate
pip install -r requirements.txt
```

---

# Useful Commands

## See commit history

```bash
git log --oneline
```

## See current remote GitHub connection

```bash
git remote -v
```

## See what changed before staging

```bash
git diff
```

## See what changed after staging

```bash
git diff --cached
```

## Undo unstaged changes to a file

```bash
git restore filename
```

## Unstage a file

```bash
git restore --staged filename
```

---

# Good Commit Message Examples

```bash
git commit -m "Add initial literacy data overview"
git commit -m "Clean literacy column names"
git commit -m "Analyze missing values in literacy dataset"
git commit -m "Create first literacy trend visualization"
git commit -m "Add poverty dataset EDA"
git commit -m "Merge literacy and poverty datasets"
git commit -m "Add correlation analysis"
```

---

# Project Commit Plan

1. Initial project setup
2. Add OWID literacy and poverty datasets
3. Update gitignore for virtual environments
4. Literacy EDA - data overview
5. Literacy EDA - missing values
6. Literacy EDA - visualizations
7. Poverty EDA - data overview
8. Poverty EDA - visualizations
9. Merge literacy and poverty datasets
10. Correlation analysis
11. Final README and project summary

---

# Important Rules

Do not commit virtual environments:

```text
.venv/
.venv-mac/
.venv-windows/
venv/
```

Do not rely on Google Drive for Git anymore.

Use GitHub as the source of truth:

```text
Windows → git push → GitHub → git pull → Mac
Mac → git push → GitHub → git pull → Windows
```

Always pull before starting work.

Always push after finishing work.
