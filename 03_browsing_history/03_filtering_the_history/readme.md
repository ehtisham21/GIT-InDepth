# 🔍 Filtering Git History – A Practical Guide ✨

Welcome! This guide will walk you through how to filter your Git commit history using different `git log` options. Whether you're new to Git or a pro, this guide gives you real-world examples and tips to help you find what you need quickly in your project's history. Let’s dive in! 🌊💻

---

## 📑 Table of Contents
- 🔍 Introduction
- 🛠️ Basic Filters
  1. `git log --oneline -3` 📄
  2. `git log --oneline --author="ehtisham21"` 👤
  3. `git log --after="2024-04-10"` 📅
  4. `git log --after="yesterday"` or `git log --after="one week ago"` 🕰️
- 📝 Content Filters
  5. `git log --oneline -S"see"` 🔍
  6. `git log --oneline -S"see" --patch` 🐛🔧
- 📏 Range Filters
  7. `git log --oneline <commit1>..<commit2>` 📈
- 📁 File Path Filters
  8. `git log --oneline <directory>` 📂
  9. `git log --oneline <file-path>` 🗂️

---

## 🔍 Introduction

Git provides powerful tools to filter commit logs based on author, date, file, keyword, and more. Mastering these filters can help you review code faster, debug efficiently, and track changes accurately.

---

## 🛠️ Basic Filters

### 1. `git log --oneline -3` 📄  
Shows the last 3 commits in a single-line format.

🔧 **Use it for:**
- Quick overviews
- Recent activity checks
- Selecting a commit to branch from

```bash
git log --oneline -3
```

📤 **Example Output:**
```
a1b2c3d Added login feature
e4f5g6h Fixed dashboard bug
i7j8k9l Updated documentation
```

---

### 2. `git log --oneline --author="ehtisham21"` 👤  
Filters commits by author name.

🔧 **Use it for:**
- Checking individual contributions
- Author-based reviews

```bash
git log --oneline --author="ehtisham21"
```

📤 **Example Output:**
```
a1b2c3d Added login feature
i7j8k9l Updated documentation
```

---

### 3. `git log --after="2024-04-10"` 📅  
Lists commits made after a specific date.

🔧 **Use it for:**
- Reviewing progress since a milestone
- Preparing for releases

```bash
git log --after="2024-04-10"
```

📤 **Example Output:**
```
commit a1b2c3d...
Author: ehtisham21
Date:   Thu Apr 12 14:23 2024

    Added login feature
```

---

### 4. `git log --after="yesterday"` or `git log --after="one week ago"` 🕰️  
Uses relative dates to filter recent commits.

🔧 **Use it for:**
- Daily/weekly review reports
- Automation in scripts

```bash
git log --after="yesterday"
git log --after="one week ago"
```

---

## 📝 Content Filters

### 5. `git log --oneline -S"see"` 🔍  
Finds commits where a specific word was added or removed in the diff.

🔧 **Use it for:**
- Tracking features by keyword
- Locating when a term was introduced

```bash
git log --oneline -S"see"
```

📤 **Example Output:**
```
a1b2c3d Added ability to see user details
e4f5g6h Refactored see functionality
```

---

### 6. `git log --oneline -S"see" --patch` 🐛🔧  
Shows diffs along with commits matching a keyword.

🔧 **Use it for:**
- Detailed debugging
- Understanding changes made to a specific feature

```bash
git log --oneline -S"see" --patch
```

📤 **Example Output:**
```
a1b2c3d Added ability to see user details
diff --git a/User.js b/User.js
+ // Feature: see user profile
```

---

## 📏 Range Filters

### 7. `git log --oneline <commit1>..<commit2>` 📈  
Shows commits between two specific commits.

🔧 **Use it for:**
- Reviewing feature development
- Comparing changes between versions

```bash
git log --oneline abc123..def456
```

---

## 📁 File Path Filters

### 8. `git log --oneline <directory>` 📂  
Shows commit history affecting a specific directory.

```bash
git log --oneline src/components/
```

---

### 9. `git log --oneline <file-path>` 🗂️  
Filters commits related to a specific file.

```bash
git log --oneline README.md
```

---

## ✅ Conclusion

Filtering Git history is a game-changer for navigating your codebase effectively. With the right filters, you can find changes faster, improve code reviews, and stay organized. Keep experimenting with these commands to make Git work smarter for you! 🚀
