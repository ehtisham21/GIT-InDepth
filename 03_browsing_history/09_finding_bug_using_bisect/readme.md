# 🐞 Finding Bugs with Git Bisect

Welcome to your step-by-step guide on how to **find bugs using Git Bisect**! 🚀 Whether you’re just starting out or an experienced developer, this guide will help you track down exactly **which commit introduced a bug** using Git’s built-in binary search. Let’s get started! 🕵️‍♂️

---

## 📚 Table of Contents

1. 🔍 Introduction  
2. 🛠️ Start Bisecting  
3. 📌 Mark Good & Bad Commits  
4. 🔄 Test & Navigate  
5. 🔚 Reset Bisect  
6. 📝 Conclusion  

---

## 🔍 Introduction

`git bisect` is a powerful tool for finding the **exact commit** that caused a bug in your code. It works by performing a **binary search** through your commit history. You simply tell Git which commit is *bad* (has the bug) and which is *good* (bug-free), and Git walks you through the rest.

---

## 🛠️ Start Bisecting

Before you begin, make sure:
- Your working directory is clean (no uncommitted changes)
- You know one commit where the bug exists (**bad**)  
- You know one earlier commit where the bug does **not** exist (**good**)

Start the bisect session:

```bash
git bisect start
```

---

## 📌 Mark Good & Bad Commits

### Mark the Bad Commit

This tells Git where the bug is currently happening:

```bash
git bisect bad
```

Usually, this is your current commit (HEAD).

---

### Mark the Good Commit

This is a commit where everything was working fine (no bug):

```bash
git bisect good ca49180
```

Replace `ca49180` with the SHA of a known good commit.

---

## 🔄 Test & Navigate Through Commits

After marking good and bad commits, Git will check out a commit halfway between them. You’ll test it and tell Git whether the bug is present.

### Example Flow

1. Git selects a midpoint commit `b20af3f`
2. You test it and see the bug:
   ```bash
   git bisect bad
   ```
3. Git selects an earlier commit `a1b2c3d`
4. You test it and the bug is gone:
   ```bash
   git bisect good
   ```

Git will repeat this process until it finds the **exact commit that introduced the bug**.

### Marking Test Results

- If the bug is present:
  ```bash
  git bisect bad
  ```

- If the bug is **not** present:
  ```bash
  git bisect good
  ```

This loop continues until Git outputs:

```
<commit-SHA> is the first bad commit
```

---

## 🔚 Reset Bisect

Once Git finds the bad commit, you should reset bisect to return to your original branch:

```bash
git bisect reset
```

This cleans up and restores your working directory to the state before you started bisecting.

---

## 📝 Conclusion

`git bisect` is a super useful tool for tracking down bugs efficiently, especially in large codebases. Instead of checking every commit manually, let Git walk you through a binary search until the problem is found. Just remember to reset when done, and you’re back on track!

Happy debugging! 🔧🐛💻
