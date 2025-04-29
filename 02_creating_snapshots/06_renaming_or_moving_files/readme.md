# 📁 Renaming or Moving Files in Git

Keeping your Git repository organized often means renaming or moving files as your project evolves. This guide shows how to do that using both standard shell commands and Git-specific tools. 🚀

---

## 📚 Table of Contents

1. Rename/Move Using `mv` Command  
2. Check Git Status  
3. Stage the Changes  
4. Use `git mv` (Alternative)  
5. Commit Your Changes  
6. Summary  

---

## 1️⃣ Rename or Move File Using `mv`

Use the `mv` command to rename or move files in your working directory. This is a basic shell command and works outside Git.

```bash
mv old-name.txt new-name.js
```

📌 **Example:**

```bash
mv file1.txt main.js
```

🧾 **What It Does:**

- Renames `file1.txt` to `main.js`.
- Or, if `new-name` includes a path, it moves the file to that location.

⚠️ *Note: This only changes the file in your local system. Git doesn’t know about it yet!*

---

## 2️⃣ Check Git Status

After renaming or moving the file, check Git’s status to see what’s changed.

```bash
git status
```

📌 **Example Output:**

```
renamed:    file1.txt -> main.js
```

This tells you Git sees the rename, but you haven’t staged it yet.

---

## 3️⃣ Stage the Renamed File

Tell Git you want to include the renamed/moved file in your next commit.

```bash
git add main.js
```

✅ **Tip:** Use `git add -A` to stage *all* changes (new, modified, and deleted files).

---

## 4️⃣ Use `git mv` (Optional but Easier)

The `git mv` command simplifies everything by renaming/moving *and* staging the file in one step.

```bash
git mv old-name.txt new-name.js
```

📌 **Example:**

```bash
git mv main.js file1.txt
```

✨ **Why use `git mv`?**

- One-step process: Rename/move and stage in one go.
- Git-friendly: Keeps track of changes properly.
- Prevents common errors with manual `mv` + `git add`.

⚠️ Make sure the destination filename doesn’t already exist to avoid overwriting.

---

## 5️⃣ Commit Your Changes

Once your changes are staged, commit them to save the update in the project history.

```bash
git commit -m "Rename file1.txt to main.js"
```

🧠 **Best Practice:** Use clear, specific commit messages so future collaborators understand what happened.

---

## ✅ Summary

| Task                        | Command                        |
|----------------------------|--------------------------------|
| Rename with `mv`           | `mv old.txt new.js`            |
| Stage manually             | `git add new.js`               |
| Rename with `git mv`       | `git mv old.txt new.js`        |
| Commit the change          | `git commit -m "Your message"` |
