# 🛠️ How to Recover a Deleted File in Git

This is your go-to guide for bringing back deleted files using Git! Whether you're just getting started or already experienced, this guide walks you through each step with easy examples and clear commands.

## 📚 Table of Contents
- 🔍 Overview
- ❌ Deleting a File
  1. `git rm <file-name>`
  2. `git commit -m "Delete <file-name>"`
- ♻️ Restoring the File
  3. `git log --oneline`
  4. `git checkout <commit-SHA> <file-name>`
- ✅ Final Steps
  5. `git status -s`
  6. `git commit -m "Restore <file-name>"`
- 📝 Summary

---

## 🔍 Overview

Accidentally deleted a file? Don’t worry! Git keeps a full history, so it’s possible to bring back removed files. This guide helps you safely delete, then recover a file using simple Git commands.

---

## ❌ Deleting a File in Git

Before learning to restore, it’s helpful to understand how deletions work in Git.

### 1. `git rm <file-name>` 🗑️

**What it does**:  
Removes the file from both your folder and Git’s tracking system.

**Why it's useful**:
- Makes the removal part of Git’s history
- Prepares the change for commit

**Example**:
```bash
git rm notes.txt
```

**Output**:
```
rm 'notes.txt'
```

---

### 2. `git commit -m "Delete notes.txt"` ✍️

**What it does**:  
Saves the file removal as a commit.

**Why it's useful**:
- Documents the deletion
- Keeps the change in Git history

**Example**:
```bash
git commit -m "Delete notes.txt"
```

**Output**:
```
[main 123abcd] Delete notes.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 notes.txt
```

---

## ♻️ Restoring a Deleted File

### 3. `git log --oneline` 📄

**What it does**:  
Shows a short list of past commits.

**Why it's useful**:
- Helps you find the commit where the file existed

**Example**:
```bash
git log --oneline
```

**Output**:
```
a642e12 Restore notes.txt
b20af3f Delete notes.txt
c1d2e3f Add notes.txt
```

---

### 4. `git checkout <commit-SHA> <file-name>` 🔑

**What it does**:  
Restores the file from a specific commit.

**Why it's useful**:
- Brings the deleted file back to your working folder

**Example**:
```bash
git checkout c1d2e3f notes.txt
```

**Output**:
```
M       notes.txt
```

---

## ✅ Final Steps

### 5. `git status -s` 📝

**What it does**:  
Checks if the file is back and ready to be committed.

**Why it's useful**:
- Verifies the restored file is staged or modified

**Example**:
```bash
git status -s
```

**Output**:
```
 M notes.txt
```

---

### 6. `git commit -m "Restore notes.txt"` 🔄

**What it does**:  
Saves the restored file as a new commit.

**Why it's useful**:
- Logs the restoration in your project’s history

**Example**:
```bash
git commit -m "Restore notes.txt"
```

**Output**:
```
[main a642e12] Restore notes.txt
 M notes.txt
```

---

## 📝 Summary

That’s it! You’ve learned how to:
- Properly delete a file in Git
- Find the commit where it was last present
- Recover the file from history
- Confirm and save the restoration

By following these steps, you can confidently manage and recover deleted files in any Git project. 🚀
