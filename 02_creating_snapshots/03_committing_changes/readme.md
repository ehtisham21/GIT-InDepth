# 📌 Committing Changes in Git – A Professional Guide

Effectively committing changes in Git is essential for maintaining a clean and understandable project history. This guide covers two common methods of committing: using an inline message and writing a detailed message through your default editor.

---

## 📚 Table of Contents

1. [Inline Commit with a Message](#1-inline-commit-with-a-message)
2. [Commit with a Detailed Message](#2-commit-with-a-detailed-message)
3. [Summary](#summary)

---

## 1. Inline Commit with a Message

For quick commits, Git allows you to include a message directly from the command line using the `-m` option. This method is ideal for simple, concise updates.

### 🔧 Syntax

```bash
git commit -m "Your descriptive commit message"
```

### 🛠 Example

```bash
git commit -m "Add homepage layout"
```

### 📝 Explanation

- `git commit`: Saves staged changes to the repository.
- `-m "message"`: Adds a brief commit message directly inline.

### ✅ Best Practices

- Use clear, meaningful messages.
- Summarize the change in the present tense (e.g., `Fix bug`, `Update styles`, `Add login page`).
- Avoid vague messages like "changes" or "updates".

---

## 2. Commit with a Detailed Message

For more complex changes, it's often better to write a detailed message explaining what was changed and why. Omitting the `-m` flag opens your system's default editor for writing a structured commit message.

### 🔧 Syntax

```bash
git commit
```

### 🛠 Example

```bash
git commit
```

### 📝 Steps

1. **Run the Commit Command:**
   - Simply use `git commit` without the `-m` flag.

2. **Write Your Commit Message:**

   - **Subject Line:** A short summary (max 50 characters).
   - **Blank Line:** Leave an empty line.
   - **Body:** Include additional context, reasoning, and technical details.

   **Example:**
   ```
   Add user authentication feature

   - Implemented user login and registration
   - Integrated JWT token-based authentication
   - Updated user model and routes for secure access
   ```

3. **Save and Exit the Editor:**

   - **Vim:**
     - Press `i` to enter insert mode.
     - Write your message.
     - Press `Esc`, type `:wq`, and hit `Enter` to save and quit.
   - **Nano:**
     - Type your message.
     - Press `Ctrl + O` to save, then `Ctrl + X` to exit.

### 📌 Why Use This Method?

- Encourages thoughtful commit messages.
- Provides context for collaborators and future maintainers.
- Ideal for large or meaningful changes.

### 🗣 Tip:
Always use the **imperative mood** in your subject lines (e.g., "Add feature" instead of "Added feature") to follow Git conventions.

---

## 📋 Summary

| Method | Command | When to Use |
|--------|---------|-------------|
| **Quick Inline Commit** | `git commit -m "message"` | For minor or simple changes |
| **Detailed Commit via Editor** | `git commit` | For complex updates that need explanation |

---

🎉 **Great work!** You now understand how to create meaningful commits in Git using both quick and detailed approaches. This is a foundational skill that enhances collaboration and makes your codebase easier to maintain.
