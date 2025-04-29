# 🔍 Visual Diff Tools with Git (Using VS Code)

Enhance your Git workflow by using a visual diff tool like **VS Code**. It helps you clearly compare changes in your codebase, making version control more intuitive and efficient. This guide shows you how to configure and use VS Code as your Git diff tool. 🛠️💻

---

## 📚 Table of Contents
1. Set Global Diff Tool ⚙️🌍  
2. Configure VS Code as Diff Tool 🔧🖥️  
3. Open Git Config File 📝📁  
4. View Unstaged Changes 🔍📄  
5. Review Staged Changes 📊✅  
**Summary** 🗂️✅

---

## ⚙️🌍 1. Set Global Diff Tool

Set your preferred visual diff tool globally so it works across all your Git repositories.

### 📌 Command
```bash
git config --global diff.tool vscode
```

### 📝 Explanation
This command tells Git to use `vscode` as the default visual diff tool system-wide.

> 💡 **Tip:** Make sure VS Code is installed and accessible in your system’s PATH.

---

## 🔧🖥️ 2. Configure VS Code as Diff Tool

Tell Git how to launch VS Code for comparing files.

### 📌 Command
```bash
git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"
```

### 📝 Explanation
This configures Git to launch VS Code in diff mode:
- `--wait` ensures Git pauses until you close VS Code.
- `$LOCAL` and `$REMOTE` refer to the two files being compared.

> 💡 **Tip:** Replace `"code"` with the full path to your VS Code binary if needed.

---

## 📝📁 3. Open Git Config File

Open your global Git configuration file to manually edit or verify your settings.

### 📌 Command
```bash
git config --global -e
```

### 📝 Explanation
This command opens `~/.gitconfig` in your default editor (VS Code, if configured).

> 💡 **Tip:** Useful for advanced edits or troubleshooting.

---

## 🔍📄 4. View Unstaged Changes

Compare changes in your working directory that haven’t been staged yet.

### 📌 Command
```bash
git difftool
```

### 📝 Explanation
This launches your configured visual diff tool to compare current file changes with the staged versions.

> 💡 **Tip:** Use `git difftool <filename>` to focus on one file.

---

## 📊✅ 5. Review Staged Changes

Before committing, visually inspect what’s staged.

### 📌 Command
```bash
git difftool --staged
```

### 📝 Explanation
This opens VS Code to compare staged changes against the last commit.

> 💡 **Tip:** Always check your staged files before committing to avoid errors.

---

## 🗂️✅ Summary

Using a visual diff tool like VS Code with Git makes version control more transparent and manageable:
- Quickly spot and understand changes
- Prevent mistakes before commits
- Keep your history clean and readable

Add it to your Git toolkit and level up your development workflow! 🚀
