### 🗂️❌ Unstaging Files in Git  
Keeping your staging area clean is important for a neat commit history. This guide walks you through how to remove files from staging using `git restore --staged`. 🛠️🚀  

---

### 📑 Table of Contents  
1. Modify a File ✏️📄  
2. Stage the File ➕📂  
3. Unstage the File 🔄❌  
**Summary 📝📋**

---

### ✏️📄 1. Modify a File  
Make a change in your working directory. This can be editing existing code or adding new content.  

📌 **Command**  
```bash
echo fishes >> moon/main.js
```

🛠️ **Example**  
```bash
echo fishes >> moon/main.js
```

📝 **Explanation**  
This command adds the word `fishes` to the end of `main.js` in the `moon` folder.  
If the file doesn’t exist, Git creates it and adds `fishes` as the first line.

💡 **Tip**  
Make small, regular changes to keep your work easy to track and debug.

---

### ➕📂 2. Stage the File  
Once you've made your changes, stage them so Git knows to include them in the next commit.  

📌 **Command**  
```bash
git add moon/main.js
```

🛠️ **Example**  
```bash
git add moon/main.js
```

📝 **Explanation**  
This adds `main.js` to the staging area, which means it’s ready to be committed.

💡 **Tip**  
Use `git add .` to stage all changes in the current folder and its subfolders.

---

### 🔄❌ 3. Unstage the File  
Changed your mind? You can unstage the file and return it to a modified-but-not-staged state.

📌 **Command**  
```bash
git restore --staged moon/main.js
```

🛠️ **Example**  
```bash
git restore --staged moon/main.js
```

📝 **Explanation**  
This removes `main.js` from the staging area, but keeps the changes in your working directory.

⚠️ **Important**  
This doesn't delete your edits—it just tells Git not to include them in the next commit.

💡 **Bonus Tip**  
To throw away the changes and reset the file to its last committed version, run:  
```bash
git restore moon/main.js
```

---
