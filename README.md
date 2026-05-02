# Git & GitHub Assessment

## Overview

This repository demonstrates the practical use of Git and GitHub. It covers repository setup, tracking changes, working with branches, and handling common errors using Git commands.

---

## Question 1: Project Initialization & First Push

### Objective

Set up a new Git project and push it to a remote repository.

### Steps

```bash
# Create project folder
mkdir my-python-project
cd my-python-project

# Initialize Git repository
git init

# Create Python file
echo "print('Hello, Git!')" > app.py

# Check repository status
git status

# Stage file
git add app.py

# Commit changes
git commit -m "Initial commit: add app.py"

# Add remote repository
git remote add origin https://github.com/your-username/my-python-project.git

# Verify remote configuration
git remote -v

# Push to remote repository
git branch -M main
git push -u origin main
```

---

## Question 2: Working with Changes and History

### Objective

Track changes and manage commit history effectively.

### Steps

```bash
# Modify file
echo "print('New Feature')" >> app.py

# Check changes
git status

# View differences
git diff

# Stage specific changes
git add -p

# Commit changes
git commit -m "Added new feature"

# Make another change
echo "print('Another change')" >> app.py

# Stage all changes
git add .

# Commit again
git commit -m "Added another change"

# View full commit history
git log

# View compact history
git log --oneline
```

---

## Question 3: Branching and Feature Development

### Objective

Work with branches to develop features independently.

### Steps

```bash
# Create a new branch
git branch feature-update

# Switch to the new branch
git checkout feature-update

# Modify file
echo "print('Feature branch code')" >> app.py

# Stage and commit changes
git add .
git commit -m "Added feature update"

# Switch back to main branch
git checkout main

# Merge feature branch
git merge feature-update

# Verify merge
git log --oneline

# Delete branch safely
git branch -d feature-update

# Create a dummy branch
git branch dummy-branch

# Force delete the branch
git branch -D dummy-branch
```

---

## Question 4: Handling Errors (Stash, Reset, Revert)

### Objective

Handle mistakes and manage unfinished work effectively.

### Steps

```bash
# Make changes without committing
echo "print('Work in progress')" >> app.py

# Stash changes including untracked files
git stash -u

# View stash list
git stash list

# Apply stashed changes
git stash apply

# Commit applied changes
git add .
git commit -m "Applied stashed changes"

# Make an incorrect commit
echo "print('Wrong code')" >> app.py
git add .
git commit -m "Wrong commit"

# Undo last commit but keep changes
git reset --soft HEAD~1

# Commit corrected changes
git add .
git commit -m "Fixed previous mistake"

# Revert last commit safely
git revert HEAD

# Verify commit history
git log --oneline
```

---

## Key Concepts

### Selective Staging

`git add -p` allows staging specific parts of changes instead of the entire file.

### Reset

`git reset` removes commits from history. It should be used carefully, especially in shared repositories.

### Revert

`git revert` creates a new commit that reverses the changes of a previous commit. This is the safest way to undo changes in a shared environment.

### Stash

`git stash` temporarily saves uncommitted changes so you can work on something else.

---

## Final Push

```bash
git push origin main
```

Only committed changes are pushed to the remote repository. Stashed or reset changes are not included. Revert creates a new commit, which will be pushed.

---

## Conclusion

This project demonstrates a complete Git workflow, including initialization, tracking changes, branching, and handling errors. It reflects best practices for maintaining clean and manageable version control history.



<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 52 50 PM" src="https://github.com/user-attachments/assets/64202c6a-54dc-4ae0-b8f9-e5858ba52e1f" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 54 47 PM" src="https://github.com/user-attachments/assets/a054649e-a44a-45c2-b316-12716e1329d1" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 54 49 PM" src="https://github.com/user-attachments/assets/1f95a32a-e35a-493c-b788-8865b48f76db" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 55 07 PM" src="https://github.com/user-attachments/assets/f97374da-f7aa-404f-a4f0-7fd3cd189848" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 56 01 PM" src="https://github.com/user-attachments/assets/aa8b4df8-8467-4bfe-abbf-15f42df1bb46" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 56 07 PM" src="https://github.com/user-attachments/assets/94de607a-003b-46b1-a31f-b26bb2e01acb" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 57 48 PM" src="https://github.com/user-attachments/assets/784ce758-8591-46b9-9183-8079fe86b919" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 58 02 PM" src="https://github.com/user-attachments/assets/6649ab8b-c3e3-497e-b9a9-c7c1564e0f8c" />
<img width="1470" height="956" alt="Screenshot 2026-05-02 at 5 59 23 PM" src="https://github.com/user-attachments/assets/e936ca61-99c8-42f8-bde0-a690bf5d9180" />

