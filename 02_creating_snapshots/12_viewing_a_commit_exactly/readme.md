### 📑 Table of Contents
1. Check Commit History 📚🔍  
2. See Commit Details 📝🔍  
3. Show Commit Differences from HEAD 🔄📊  
4. Show File Content at a Commit 📂🖥️  
5. List Files/Folders in a Commit 📋📁  
6. View File Metadata in Commit via `ls-tree` 🗂️🔍  
**Summary 📝✅**

---

### 📚🔍 1. Check Commit History  
To quickly review past changes, display a simplified view of the commit history.  

📌 **Command**  
```bash
git log --oneline
```

🛠️ **Example**  
```bash
git log --oneline
```

📝 **What It Does**  
Shows each commit on a single line with a short hash and message.  
**Use Case:** Quickly find a commit to investigate.  

📋 **Sample Output**  
```
6973451 Implement user authentication feature  
af7a9a4 Update .gitignore to exclude bin directory  
01c9746 Add binary files to bin directory  
```

---

### 📝🔍 2. See Commit Details  
To view the full details of a specific commit, use `git show`.  

📌 **Command**  
```bash
git show <commit-id>
```

🛠️ **Example**  
```bash
git show 6973451
```

📝 **What It Does**  
Displays the commit’s metadata (author, date, message) and all changes.  
**Use Case:** Inspect exactly what changed in a commit.  

📋 **Sample Output**  
```
commit 6973451e...  
Author: Jane Doe <jane.doe@example.com>  
Date:   Mon Aug 30 14:22:35 2023 -0400  

    Implement user authentication feature  

diff --git a/src/auth.js b/src/auth.js  
new file mode 100644  
index 0000000..e69de29  
```

---

### 🔄📊 3. Show Commit Differences from HEAD  
Use `HEAD~<n>` to go back n commits and view the changes from that commit.  

📌 **Command**  
```bash
git show HEAD~<number>
```

🛠️ **Example**  
```bash
git show HEAD~2
```

📝 **What It Does**  
Displays the changes made two commits before the latest commit.  
**Use Case:** Look back at earlier modifications without needing the exact hash.  

📋 **Sample Output**  
```
commit af7a9a4e...  
Author: John Smith <john.smith@example.com>  
Date:   Sun Aug 29 10:15:20 2023 -0400  

    Update .gitignore to exclude bin directory  

diff --git a/.gitignore b/.gitignore  
+bin/  
```

---

### 📂🖥️ 4. Show File Content at a Commit  
Use `git show` with a commit ID and file path to see a file’s contents at that commit.  

📌 **Command**  
```bash
git show <commit-id>:<file-path>
```

🛠️ **Example**  
```bash
git show af7a9a4:.gitignore  
git show 01c9746:bin/app.bin
```

📝 **What It Does**  
Displays the state of the file at that specific commit.  
**Use Case:** Retrieve an earlier version of a file without checking out.  

📋 **Sample Output**  
```bash
# Content of .gitignore  
bin/  

# Content of bin/app.bin  
Binary file content...
```

---

### 📋📁 5. List Files/Folders in a Commit  
Get a snapshot of the file structure in a specific commit using `ls-tree`.  

📌 **Command**  
```bash
git ls-tree <commit>
```

🛠️ **Example**  
```bash
git ls-tree HEAD~1
```

📝 **What It Does**  
Lists all files and folders in a commit one step behind the current HEAD.  
**Use Case:** Analyze repo structure at an earlier point.  

📋 **Sample Output**  
```
100644 blob e69de29b...    .gitignore  
100644 blob d95f3adf...    README.md  
```

---

### 🗂️🔍 6. View File Metadata in Commit via `ls-tree`  
Use `ls-tree` with a file path to see file metadata (mode, type, blob ID) for a given commit.  

📌 **Command**  
```bash
git ls-tree <commit>:<file-path>
```

🛠️ **Example**  
```bash
git ls-tree HEAD~1:.gitignore
```

📝 **What It Does**  
Shows info like blob hash and file permissions for that file at the commit.  
**Use Case:** Useful for debugging or low-level inspection of file history.  

📋 **Sample Output**  
```
100644 blob d95f3adf...    .gitignore  
```
