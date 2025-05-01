# Viewing the History of a File in Git 🕵️‍♂️📄

Welcome! This guide will help you learn how to view the history of a specific file in your Git project. Whether you're debugging an issue or trying to understand how a file has evolved, this will show you how to track changes, who made them, and when. Let’s jump in! 🚀

---

## 📑 Table of Contents
- 🔍 Introduction  
- 🛠️ Viewing File History  
  1. `git log <file-name>`  
  2. `git log --oneline <file-name>`  
- 📝 Conclusion  

---

## 🔍 Introduction

Git makes it easy to track the history of any file in your project. By reviewing a file's past commits, you can understand what changes were made, when they happened, and who made them. This is useful for debugging, reviewing code, or understanding project decisions.

---

## 🛠️ Viewing File History

The `git log` command helps you explore the changes made to a file over time. Let’s look at two commonly used variations.

---

### 1. `git log <file-name>` 📄

**What It Does:**  
Shows the full commit history for a specific file, including details like author, date, commit message, and commit hash.

**Key Features:**  
- 🧾 Full commit messages  
- 👤 Shows who made the change  
- 🕒 Includes date and time of each change  

**Example Command:**
```bash
git log src/App.js
```

**Sample Output:**
```
commit a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9t0
Author: ehtisham21 <*****@gmail.com>
Date:   Tue Apr 30 12:47:34 2024 +0500

    Refactored App component for better performance

commit e4f5g6h7i8j9k0l1m2n3o4p5q6r7s8t9u0v1w2x3
Author: Jane Doe <jane.doe@example.com>
Date:   Mon Apr 29 09:15:30 2024 +0500

    Fixed routing bug in App.js

commit z9y8x7w6v5u4t3s2r1q0p9o8n7m6l5k4j3i2h1g0
Author: John Smith <john.smith@example.com>
Date:   Sun Apr 28 14:23:45 2024 +0500

    Added new feature to App.js
```

**Use Cases:**  
- 🔎 See what changes were made to a file  
- 🐞 Find when a bug was introduced  
- ✅ Review file-specific changes during code reviews  
- 📚 Document a file’s development history  

---

### 2. `git log --oneline <file-name>` 🔍

**What It Does:**  
Displays a simplified view with one line per commit — showing the short commit hash and the first line of the commit message.

**Key Features:**  
- 📄 Clean, minimal output  
- 🔢 Shortened commit hashes  
- 🚀 Easy to scan quickly  

**Example Command:**
```bash
git log --oneline src/App.js
```

**Sample Output:**
```
a1b2c3d Refactored App component for better performance  
e4f5g6h Fixed routing bug in App.js  
z9y8x7w Added new feature to App.js  
```

**Use Cases:**  
- ⚡ Quickly review a file’s change history  
- 🧭 Navigate recent changes with less clutter  
- 🔁 Compare frequency and types of changes  

---

## 📝 Conclusion

By using `git log` with a file path, you can get a clear picture of how that file has evolved over time. Whether you need detailed commit information or a quick summary, these commands are essential for tracking changes and understanding your codebase better.

Happy coding! 💻✨
