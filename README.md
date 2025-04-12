# DevOps Task 4 – Git Workflow

This project demonstrates a complete Git workflow with best practices including branching, pull requests, tagging, and documentation.

📁 STEP-BY-STEP EXECUTION
1. Project Initialization
a. Create Local Folder
mkdir devops-task4
cd devops-task4

b. Initialize Git
git init

2. Create Remote GitHub Repo
Go to GitHub

Click on ➕ ➝ New Repository

Repository name: devops-task4

Set visibility to Public or Private as per your preference.

Click Create Repository

Copy the repo URL (either HTTPS or SSH)

3. Link Local Repo to Remote
git remote add origin https://github.com/yourusername/devops-task4.git


4. Create Initial Files
a. README.md
# DevOps Task 4 – Git Workflow

This project demonstrates a complete Git workflow with best practices including branching, pull requests, tagging, and documentation.

b. .gitignore
# Ignore Python, Node, logs, system files, etc.
*.log
node_modules/
.env
__pycache__/
.DS_Store

c. Add Files & Commit
git add .
git commit -m "Initial commit with README and .gitignore"

d. Push to Main
git branch -M main
git push -u origin main

5. Create Branches
git checkout -b dev
git push -u origin dev

git checkout -b feature/docs
git push -u origin feature/docs

6. Add Features in Branches
In feature/docs:
Add a file TASK_DETAILS.md

# Git Workflow in DevOps

## Branches:
- `main`: production-ready
- `dev`: staging
- `feature/docs`: documentation-related updates

## Pull Requests
All changes must go via PR into `dev` or `main`


git add TASK_DETAILS.md
git commit -m "Add task documentation"
git push

7. Create Pull Requests
Go to your GitHub repo.

Click Pull requests > New Pull Request

Set:

From: feature/docs

Into: dev

Click Create Pull Request

Add title & description → Click Merge

Repeat similarly when merging dev into main.

8. Tagging Commits
After stable changes in main, tag it:

git checkout main
git pull
git tag -a v1.0 -m "Stable version 1"
git push origin v1.0


9. Git Stash Demo (Optional Learning)
# Make unsaved changes
echo "Test changes" > temp.txt

# Stash them
git stash

# Later recover
git stash pop


10. Document All Tasks in Markdown
Create a DOCUMENTATION.md file:

# Git Workflow Documentation

## Steps Covered:
- Init repo
- Setup remote
- Create branches
- Use pull requests
- Add .gitignore
- Use tags
- Markdown docs

## Git Commands Used:
- git init, git add, git commit, git push
- git checkout -b
- git merge, git pull
- git tag, git stash

✅ FINAL DELIVERABLES CHECKLIST

Item	Completed?
Git repo with commits	    ✅
Branching (main/dev/feat)	✅
Pull request used	        ✅
README.md created	        ✅
.gitignore added	        ✅
Tags used	                ✅
Markdown documentation	    ✅