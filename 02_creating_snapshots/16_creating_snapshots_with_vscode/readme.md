# 📘 Version Control in VS Code: Take Snapshots with Git

Using **Visual Studio Code's built-in Git tools**, you can create clear project snapshots at different stages, making your development process more organized and trackable. This guide walks you through the process of setting up Git in VS Code, creating commits (snapshots), and comparing project changes visually. 🚀🛠️

---

## 📋 Steps Overview:
1. Open your project in VS Code  
2. Initialize Git repository (if needed)  
3. Stage files for commit  
4. Make a commit (create snapshot)  
5. View commit history  
6. Create commits at meaningful stages  
7. Compare snapshots to track changes  

---

## 🖥️ Open Your Project in VS Code

Start by launching VS Code and opening your project folder:

- Open VS Code
- Use **File > Open Folder** to select your project, or run `code .` in your terminal from the project directory.

---

## 🛠️ Initialize Git Repository

If you haven’t already:

```bash
git init
```

This sets up Git in your folder. It creates a hidden `.git` folder to track all version control changes.  
💡 *Tip: Add a `.gitignore` file to avoid tracking unnecessary files.*

---

## ➕ Stage Files for Commit

Now tell Git which files to include in your next snapshot:

1. Open the **Source Control** panel from the sidebar (Git icon).
2. Under **Changes**, click ➕ next to files you want to stage, or click **Stage All Changes**.

📘 *Staging means selecting which changes to save in your next snapshot.*

---

## ✍️ Make a Commit (Create Snapshot)

Once files are staged:

1. In the **Message** box, write a short description of what you changed.
2. Press **Ctrl+Enter** (Windows/Linux) or **Cmd+Enter** (Mac), or click the ✔️ icon to commit.

💡 *Use clear, meaningful messages like: `Add login form validation` or `Fix typo in readme`.*

---

## 📜 View Commit History

To see past snapshots:

1. In the **Source Control** panel, click the clock icon 🕒.
2. Browse the list of previous commits with messages, dates, and changes.

🧠 *Clicking on a commit lets you view exactly what changed.*

---

## 📸 Create Snapshots Frequently

Every time you finish a feature, fix a bug, or make progress:

- Repeat the **stage + commit** steps.
- Optionally, **tag important commits**:

```bash
git tag -a v1.0 -m "Initial release"
```

✅ Frequent commits help you revert changes, understand project evolution, and stay organized.

---

## 🔍 Compare Changes Between Snapshots

To view what changed between two points:

1. In commit history, select any two commits.
2. Right-click and choose **Compare with Selected**.
3. VS Code will open a side-by-side diff showing what was added, changed, or removed.

💡 *VS Code highlights differences visually, making it easy to track progress or debug.*

---

By following these steps, you can take full advantage of Git in VS Code to manage your project's history, create snapshots at key stages, and compare changes with ease.  
Consistent use of commits = a clean and powerful project timeline. ✅✨
