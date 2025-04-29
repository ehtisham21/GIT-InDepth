### 🔄✨ Discard Local Changes in Git  
Keeping a clean working directory is key to an efficient Git workflow. This guide explains how to undo local changes to tracked files and remove untracked files from your repository using `git restore` and `git clean`. 🛠️🚀  

---

### 📑 Table of Contents  
1. Undo Changes to a Tracked File ✏️🔄  
2. Create a New File and Add Content 🆕📄  
3. Check the Status of Untracked Files 🔍📊  
4. Remove Untracked Files Permanently 🗑️🚫  
**Summary 📝📋**

---

### ✏️🔄 1. Undo Changes to a Tracked File  
Sometimes you may want to undo changes to a file you’ve already tracked in Git. This section covers how to reset the file back to its last committed version.  

📌 **Step 1: Make Changes to a File**  
Modify a tracked file, like adding text to `moon/main.js`.  

📌 **Command**  
```bash
echo fishes >> moon/main.js
```

🛠️ **Example**  
```bash
echo fishes >> moon/main.js
```

📝 **Explanation**  
This appends the word `fishes` to the `main.js` file inside the `moon` directory. If the file doesn't exist, it gets created with the content `fishes`.

📌 **Step 2: Stage the Changes**  
Add the file to the staging area for committing.  

📌 **Command**  
```bash
git add moon/main.js
```

🛠️ **Example**  
```bash
git add moon/main.js
```

📝 **Explanation**  
This stages the changes made to `main.js` so they’ll be included in your next commit.

📌 **Step 3: Undo Staged Changes**  
To undo the staged changes and revert to the last committed version, use the `git restore --staged` command.  

📌 **Command**  
```bash
git restore --staged moon/main.js
```

🛠️ **Example**  
```bash
git restore --staged moon/main.js
```

📝 **Explanation**  
This command removes `main.js` from the staging area, but the changes stay in your working directory. They’re just no longer staged for the next commit.  

⚠️ **Note**  
This doesn’t remove your changes—it just unstages them.

💡 **Tip**  
To completely discard all local changes and return the file to its last committed state, run:  
```bash
git restore moon/main.js
```

---

### 🆕📄 2. Create a New File and Add Content  
Creating new files is common, but sometimes you may want to remove them from the repository if they’re no longer needed. Here's how you handle that.  

📌 **Step 1: Create a New File**  
Create a new file and add some content to it. For example, create `file3.js` in the `moon` directory and write "Hello".  

📌 **Command**  
```bash
echo Hello > moon/file3.js
```

🛠️ **Example**  
```bash
echo Hello > moon/file3.js
```

📝 **Explanation**  
This creates a new file called `file3.js` inside the `moon` directory with the content `Hello`. If the file already exists, it will be overwritten.

---

### 🔍📊 3. Check the Status of Untracked Files  
Once new files are created, you can check if they’re tracked by Git. Untracked files are those that Git isn’t keeping track of yet.  

📌 **Command**  
```bash
git status -s
```

🛠️ **Example**  
```bash
git status -s
```

📝 **Explanation**  
This shows the status of your repository. Untracked files are marked with `??`.  

💡 **Tip**  
Checking the status regularly helps manage which files are tracked and which should be ignored.

---

### 🗑️🚫 4. Remove Untracked Files Permanently  
If there are untracked files you no longer need, you can remove them to keep your repository clean using `git clean`.  

📌 **Step 1: View Help for `git clean`**  
Before removing files, see the available options by using the `-h` flag.  

📌 **Command**  
```bash
git clean -h
```

🛠️ **Example**  
```bash
git clean -h
```

📝 **Explanation**  
This displays help information for `git clean`, explaining the available options.

📌 **Step 2: Remove Untracked Files**  
To delete an untracked file, use the `--force` flag to remove it without confirmation.  

📌 **Command**  
```bash
git clean --force moon/file3.js
```

🛠️ **Example**  
```bash
git clean --force moon/file3.js
```

📝 **Explanation**  
This command permanently deletes `file3.js` from the `moon` directory.

⚠️ **Warning**  
Be cautious with `git clean`—it deletes files permanently, and there’s no confirmation prompt. Make sure you really want to remove them.

💡 **Tip**  
To preview which files would be deleted without actually removing them, use the `-n` flag:  
```bash
git clean -n moon/file3.js
```

📝 **Explanation**  
This shows which files would be deleted by `git clean` without removing them. It’s a helpful safety check.

---
