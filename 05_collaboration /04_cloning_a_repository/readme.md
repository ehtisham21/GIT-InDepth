# 📦 Cloning a GitHub Repository and Exploring Remote Setup

Follow these steps to clone a repository and understand how Git handles remotes and branches.

---

## 💻 Step 1: Open Terminal or Git Bash

- On **Linux/macOS**: Open your Terminal.
- On **Windows**: Launch **Git Bash**.
- Navigate to the folder where you want the project to be downloaded.

```bash
cd path/to/your/folder
```

---

## 📥 Step 2: Clone the Repository with a Custom Name

Use the `git clone` command followed by the repository URL, and specify a name for your local folder.

```bash
git clone https://github.com/hashimthepassionate/mars.git MarsProject
```

> This command creates a new local folder called `MarsProject` with the contents of the `mars` repository.

---

## 📂 Step 3: Enter the Cloned Directory

Switch into the project directory:

```bash
cd MarsProject
```

---

## 🌐 Step 4: Understand Remote Branches and `origin`

- `origin`: The default name Git gives to the remote you cloned from.
- `origin/main`: The `main` branch on the remote repository.
- `origin/HEAD`: A pointer indicating the default branch of the remote (usually `main` or `master`).

> When cloning, Git automatically sets up your local `main` to track `origin/main`.

---

## 🔍 Step 5: Check Remote Repository Info

To see the remotes connected to your local project, run:

```bash
git remote -v
```

You’ll see something like:

```text
origin  https://github.com/hashimthepassionate/mars.git (fetch)
origin  https://github.com/hashimthepassionate/mars.git (push)
```

> This confirms the link between your local project and the remote GitHub repository.

---
