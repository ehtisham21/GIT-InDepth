**# 🔍✨ How to View Git Commit History

Understanding your Git commit history is crucial for tracking changes, working with others, and keeping a clear timeline of your project. This guide walks you through different ways to check your commit history using the `git log` command, with easy explanations and examples. 🚀🛠️

---

## 📑 Table of Contents

1. Full Commit History 📚  
2. Compact View of Commit History 📝  
3. Oldest-to-Newest Commit View 🔄  
4. Summary ✅

---

## 📚 1. Full Commit History

To see all details about each commit, use the basic `git log` command.

### 📌 Command
```bash
git log
```

### 🛠️ Example
```bash
git log
```

### 💬 What It Shows
- **Commit Hash**: Unique ID for the commit  
- **Author**: Who made the commit  
- **Date**: When the commit was made  
- **Message**: What changes were made

### 🧾 Sample Output
```
commit e1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p7q8r9s0
Author: Jane Doe <jane.doe@example.com>
Date:   Mon Aug 30 14:22:35 2023 -0400

    Add user login functionality
```

### 🧠 Summary
- Commit made by **Jane Doe** on **August 30, 2023**  
- Message: **"Add user login functionality"**

---

## 📝 2. Compact View of Commit History

Want a cleaner summary? Use `--oneline` to show one commit per line.

### 📌 Command
```bash
git log --oneline
```

### 🛠️ Example
```bash
git log --oneline
```

### 💬 What It Shows
- Shortened commit ID  
- Short message about the change

### 🧾 Sample Output
```
e1a2b3c Add user login functionality
d4e5f6g Fix payment bug
a7b8c9d Update README file
```

### 🧠 Summary
Great for quickly browsing changes without too much detail.

> 💡 **Tip:** Use this when you want a fast overview of project changes.

---

## 🔄 3. Show Commits from Oldest to Newest

Use `--reverse` with `--oneline` to see commits in the order they were made.

### 📌 Command
```bash
git log --oneline --reverse
```

### 🛠️ Example
```bash
git log --oneline --reverse
```

### 💬 What It Shows
- A simple, one-line-per-commit view  
- Starts from the **earliest** commit

### 🧾 Sample Output
```
a7b8c9d Update README file
d4e5f6g Fix payment bug
e1a2b3c Add user login functionality
```

### 🧠 Summary
- Lets you trace how your project started and grew over time  
- Helpful for learning the full journey of your code

---

## ✅ Summary

| Command | Purpose |
|--------|---------|
| `git log` | View full commit details |
| `git log --oneline` | View a quick summary of commits |
| `git log --oneline --reverse` | View commits from oldest to newest |

Use these options to stay on top of your project history, whether you're reviewing your own work or collaborating with others. 🧠💻
