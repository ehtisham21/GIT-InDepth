# 🔍 Viewing a Git Commit

Welcome to this guide on how to inspect commits using the `git show` command! Whether you're experienced with Git or just getting started, this guide offers practical examples and clear explanations to help you view and understand individual commits in your repository.

---

## 📑 Table of Contents
- 🔍 Introduction  
- 🛠️ How to View Commit Details  
  1. `git show HEAD~2`  
  2. `git show HEAD~2 --name-only`  
  3. `git show HEAD~2 --name-status`  
- 📝 Conclusion

---

## 🔍 Introduction

Git’s `git show` command lets you view detailed information about a specific commit. This includes the commit message, author, date, and changes made. It’s especially helpful for code reviews, debugging, and understanding your project’s history.

---

## 🛠️ How to View Commit Details

Below are the most common ways to use `git show`, along with explanations and examples.

---

### 1. `git show HEAD~2` 📄

**What it does:**  
Displays complete details about the commit two steps before the current one.

**Includes:**
- Commit message
- Author and date
- Code changes (diffs)

**Explanation:**  
`HEAD~2` refers to the commit that’s two steps behind the current HEAD. This command is helpful when reviewing or debugging earlier changes.

**Example Command:**
```bash
git show HEAD~2
```

**Example Output:**
```
commit 06735275dd31d9d3e20a608bcf821fc3a93550c5
Author: Muhammad Hashim <*****@gmail.com>
Date:   Tue Apr 30 12:47:34 2024 +0500

    Added user authentication feature

diff --git a/src/Auth.js b/src/Auth.js
index e69de29..0d1d7fc 100644
--- a/src/Auth.js
+++ b/src/Auth.js
@@ -0,0 +1,10 @@
+// Authentication module
+import React from 'react';
+
+function Auth() {
+    // Authentication logic
+}
+
+export default Auth;
```

**Use Cases:**
- Perform a detailed review of a commit
- Debug recent issues
- Track feature implementation

---

### 2. `git show HEAD~2 --name-only` 👤

**What it does:**  
Shows only the names of files affected by the commit.

**Includes:**
- File paths
- No code differences

**Explanation:**  
Use this to quickly check which files were modified without diving into the actual changes.

**Example Command:**
```bash
git show HEAD~2 --name-only
```

**Example Output:**
```
src/Auth.js
src/UserProfile.js
README.md
```

**Use Cases:**
- Identify files changed in a commit
- Use in automation/scripts
- Perform quick audits

---

### 3. `git show HEAD~2 --name-status` 🗂️

**What it does:**  
Shows the names of the changed files **along with** their status (added, modified, or deleted).

**Includes:**
- File names
- Change types (A = added, M = modified, D = deleted)

**Explanation:**  
This gives a concise summary of what happened to each file, which is useful for code reviews or summaries.

**Example Command:**
```bash
git show HEAD~2 --name-status
```

**Example Output:**
```
M	src/Auth.js
A	src/UserProfile.js
D	src/OldComponent.js
```

**Use Cases:**
- Summarize file changes
- Quickly assess impact
- Improve project tracking

---

## 📝 Conclusion

The `git show` command is a powerful tool for exploring past changes in your Git project. Whether you need full details or just a summary of affected files, it has flexible options to support your workflow.
