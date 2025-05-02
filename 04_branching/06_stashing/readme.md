# Git Stashing 🗃️✨

Welcome to your go-to guide for mastering Git Stashing! 🚀 Whether you're an experienced developer or just getting started, this documentation breaks down Git's stashing feature with clear explanations, hands-on examples, and practical tips. Learn how to save and manage uncommitted changes like a pro. Let’s get started! 🧠💻

---

## 📑 Table of Contents

- 📦 What is Stashing?
- 🔍 Introduction
- 🛠️ Step-by-Step Guide
  1. Switch to the Bugfix Branch 🔄  
  2. Make Changes ✏️  
  3. Try Switching Branches Without Committing ❌  
  4. Save Changes with Stash 📦  
  5. Create a New File 🆕  
  6. Stash New Changes 📦  
  7. View All Stashes 👀  
  8. Switch Back to the Master Branch 🔙  
  9. Apply a Specific Stash 🔧  
  10. Remove a Specific Stash ❌  
  11. Clear All Stashes 🗑️  
- 🔄 Bonus Tips
- 📝 Wrap-Up

---

## 🔍 Introduction

In software development, you may need to pause your work and switch contexts without committing unfinished changes. Git’s **stash** command lets you safely store those modifications and revisit them later. This feature is especially useful when managing multiple tasks, fixing urgent bugs, or experimenting without cluttering commit history. Let's walk through how to stash, manage, and restore your changes effectively.

---

## 🛠️ Step-by-Step Guide

### 1. Switch to the Bugfix Branch 🔄

Change your working branch to start fixing a bug.

```bash
git switch bugfix
```

**Use Case:**  
- Isolate bug fixes from the main codebase  
- Easily manage multiple features or fixes

---

### 2. Make Changes ✏️

Edit your code. For example, add a line to `audience.txt`.

```bash
echo Hello >> audience.txt
```

**Use Case:**  
- Implement features  
- Fix bugs

---

### 3. Try Switching Branches Without Committing ❌

Attempt to switch to another branch. Git blocks the action to prevent loss.

```bash
git switch master
```

**Output:**

```
error: Your local changes to the following files would be overwritten by checkout:
    audience.txt
Please commit your changes or stash them before you switch branches.
Aborting
```

**Use Case:**  
- Avoid overwriting uncommitted changes

---

### 4. Save Changes with Stash 📦

Store current changes with a message.

```bash
git stash push -m "Added Hello to audience.txt"
```

**Use Case:**  
- Pause work and return later  
- Keep your working directory clean

---

### 5. Create a New File 🆕

Add a new file and check its status.

```bash
echo Hi > file.txt
git status -s
```

**Output:**

```
?? file.txt
```

**Use Case:**  
- Start tracking new project files

---

### 6. Stash New Changes 📦

Stash all modifications including untracked files.

```bash
git stash -am "Stashing new file and other changes"
```

**Use Case:**  
- Save both tracked and untracked changes temporarily

---

### 7. View All Stashes 👀

List all stored stashes.

```bash
git stash list
```

**Output:**

```
stash@{0}: On bugfix: Stashing new file and other changes
stash@{1}: On bugfix: Added Hello to audience.txt
```

**Use Case:**  
- Keep track of saved work-in-progress

---

### 8. Switch Back to the Master Branch 🔙

Return to the master branch.

```bash
git switch master
```

**Use Case:**  
- Resume work on the main project branch

---

### 9. Apply a Specific Stash 🔧

Preview and apply a particular stash.

```bash
git stash show 1
git stash apply 1
```

**Output (Show):**

```
 audience.txt | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```

**Output (Apply):**

```
Changes not staged for commit:
  modified:   audience.txt
```

**Use Case:**  
- Apply only the relevant stash to your working directory

---

### 10. Remove a Specific Stash ❌

Delete a specific stash.

```bash
git stash drop 1
```

**Output:**

```
Dropped refs/stash@{1}
```

**Use Case:**  
- Clean up your stash list

---

### 11. Clear All Stashes 🗑️

Remove all saved stashes at once.

```bash
git stash clear
```

**Use Case:**  
- Start fresh by wiping the stash list

---

## 🔄 Bonus Tips

Here are some power tips to improve your stash workflow:

- **View stash details with file changes:**

  ```bash
  git stash list --stat
  ```

- **Apply and delete in one step:**

  ```bash
  git stash pop
  ```

- **Create a new branch from a stash:**

  ```bash
  git stash branch fix-from-stash
  ```

- **Preview stash changes without applying:**

  ```bash
  git stash show -p stash@{0}
  ```

- **Stash including untracked files:**

  ```bash
  git stash push -u -m "Stashing everything"
  ```

- **Apply stash to a different branch:**

  ```bash
  git switch other-branch
  git stash apply stash@{0}
  ```

- **Use Git GUI Tools (e.g. GitLens):**  
  Tools like GitLens in VS Code let you view, apply, and delete stashes visually.

---

## 📝 Wrap-Up

Git stashing is a powerful way to manage your uncommitted work. With a few simple commands, you can save progress, switch tasks, and return exactly where you left off—without cluttering your history. Use these techniques to streamline your workflow and stay organized.
