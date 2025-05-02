# Branch Comparison Guide 🔄🌿

Welcome! This guide walks you through how to **compare Git branches** with real commands and examples. Whether you’re new to Git or an experienced developer, this readme will help you clearly understand differences between branches. Let’s get started! 🚀

## 📚 Table of Contents

- 🔍 Overview
- 🔄 Comparing Branches
  1. Switch to the Main Branch
  2. View Commits Not in Main
  3. See File Changes Between Branches
  4. Use Shortcuts to Compare Branches
    - a. Diff Current with Another Branch
    - b. Show Only Changed File Names
    - c. Show File Status (Modified, Added, Deleted)
- 💡 Extra Tips
- 📝 Summary

---

## 🔍 Overview

Git branches allow developers to work on features, fixes, or experiments in isolation. Comparing branches is important to track what changed, review code, and prepare for merging. This guide covers essential commands to compare Git branches confidently.

---

## 🔄 Comparing Branches

Below are commands and examples to help you compare changes between branches.

### 1. Switch to the Main Branch 🔁

**Why:** Ensures you’re on the base branch for comparison.

**Command:**
```bash
git switch master
```

**Example Output:**
```
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
```

**Use Cases:**
- Set `master` as the comparison base.
- Keep a clean and stable workspace.

---

### 2. View Commits Not in Master 📋

**Why:** Shows which commits exist in the other branch but not in `master`.

**Command:**
```bash
git log --oneline master..bugfix
```

**Example Output:**
```
11deb71 (bugfix) Fixed new issue
e2f7a41 Minor bug fix
```

**Use Cases:**
- See what's been done in `bugfix` that’s not in `master`.
- Prepare for code reviews or merging.

---

### 3. See File Changes Between Branches 📝

**Why:** Shows the exact line-level changes between branches.

**Command:**
```bash
git diff master..bugfix
```

**Example Output:**
```diff
diff --git a/audience.txt b/audience.txt
index 4cfef55..c01b824 100644
--- a/audience.txt
+++ b/audience.txt
@@ -1,4 +1,16 @@
 AUDIENCE

 This course is for anyone who wants to learn Git.
-No prior experience is required.
+No prior experience is required.
+
+Welcome to venus bugfix branch
+Another new changes
```

**Use Cases:**
- Deep dive into what changed in files.
- Debug or write change logs.

---

### 4. Use Shortcuts to Compare Branches 🔍

#### a. Diff Current with Another Branch

**Command:**
```bash
git diff bugfix
```

**Example Output:** (same as above)

**Use Cases:**
- Faster comparison from current branch.

---

#### b. Show Only Changed File Names 📂

**Command:**
```bash
git diff --name-only bugfix
```

**Example Output:**
```
audience.txt
login.js
logout.js
```

**Use Cases:**
- Know which files changed without details.
- Useful for summaries or scripts.

---

#### c. Show File Change Status 📋

**Command:**
```bash
git diff --name-status bugfix
```

**Example Output:**
```
M       audience.txt
A       new-feature.js
D       obsolete.js
```

**Use Cases:**
- See how files changed: Modified (M), Added (A), Deleted (D).
- Useful for code reviews or deployment prep.

## 📝 Summary

Comparing branches is a critical skill in Git that helps you track, understand, and manage code changes. With the commands above, you can effectively compare branches, review code, and prepare for safe merges.

Happy coding! 💻✨
