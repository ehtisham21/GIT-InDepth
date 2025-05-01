# 🕵️‍♂️ Finding Out Who Changed a Line with Git Blame

Want to know who changed a line in your code? This guide makes it easy! Whether you're reviewing code, fixing bugs, or just curious, `git blame` helps you see who last touched each line of a file. Let’s walk through it step by step.

---

## 📚 Table of Contents
- 🔍 What is Git Blame?
- 📄 Blame the Whole File
  1. `git blame <file-name>`
- 📜 Blame Specific Lines with Email Info
  2. `git blame -e -L <start>,<end> <file-name>`
- ✅ When to Use Git Blame
- 📝 Summary

---

## 🔍 What is Git Blame?

`git blame` shows who last changed each line in a file — including their name, commit ID, and the time of change. It’s useful when:
- Reviewing code
- Debugging issues
- Understanding how code evolved

---

## 📄 Blame the Whole File

### 1. `git blame <file-name>`

**What it does**:  
Shows who changed every line in a file, along with the commit hash, author name, and time.

**Example**:
```bash
git blame audience.txt
```

**Output**:
```
a1b2c3d4 (Jane Doe 2024-04-30 12:47:34 +0500 1) Introduction to the audience section.
e4f5g6h7 (John Smith 2024-04-29 09:15:30 +0500 2) This line explains the target demographics.
z9y8x7w6 (Jane Doe 2024-04-28 14:23:45 +0500 3) Additional details about audience engagement.
```

**Why it’s helpful**:
- Shows who changed what and when
- Helps trace bugs or logic changes
- Useful in code reviews

---

## 📜 Blame Specific Lines + Emails

### 2. `git blame -e -L <start>,<end> <file-name>`

**What it does**:  
Limits blame output to specific lines and adds email addresses.

**Options**:
- `-e`: shows the email of the author
- `-L <start>,<end>`: limits output to a specific line range

**Example**:
```bash
git blame -e -L 1,2 audience.txt
```

**Output**:
```
a1b2c3d4 (Jane Doe <jane.doe@example.com> 2024-04-30 12:47:34 +0500 1) Introduction to the audience section.
e4f5g6h7 (John Smith <john.smith@example.com> 2024-04-29 09:15:30 +0500 2) This line explains the target demographics.
```

**Why it’s helpful**:
- Focuses on only the part of the file you care about
- Lets you find who worked on specific logic
- Useful in big files

---

## ✅ When to Use Git Blame

- 🔍 **Code Reviews**: Check who added or changed a piece of logic
- 🐛 **Debugging**: Find out who introduced a bug
- 📜 **Documentation**: Understand the history of a file
- 🤝 **Team Collaboration**: Talk to the right person about a section of code

---

## 📝 Summary

`git blame` is a simple but powerful tool to trace code changes down to each line. Whether you're fixing bugs or reviewing contributions, it helps you see the full story behind your code.
