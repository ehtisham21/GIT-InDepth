# View Git History in Visual Studio Code (VS Code)

This guide will help you explore the Git history of your project directly within Visual Studio Code (VS Code). Whether you're new to Git or just looking for a faster way to inspect your repository’s changes, this guide covers everything you need — from setup to commit comparisons.

## 📂 Table of Contents
- Introduction  
- Steps to Browse Git History  
  1. Open VS Code  
  2. Load Your Project  
  3. Open Source Control  
  4. View Commit History  
  5. Browse Commits  
  6. Compare Changes  
  7. View File-Specific History  
- Tips for a Better Experience  
- Conclusion  

## 🔍 Introduction  
VS Code is a lightweight editor with strong Git integration. It allows you to manage repositories, review commit logs, and track changes — all without leaving your editor. This guide walks you through how to use these Git features efficiently.

## 🛠️ Steps to Browse Git History

### 1. Open VS Code  
Start by launching Visual Studio Code.  
- **From Desktop**: Click the VS Code icon.  
- **From Terminal**: Use `code .` after navigating to your project folder:
```bash
cd path/to/project
code .
```

### 2. Load Your Project  
Open the folder that contains your Git repository.  
- **Via Menu**: File > Open Folder...  
- **Drag & Drop**: Drag the folder into the VS Code window.

### 3. Open Source Control  
Go to the Source Control panel to access Git tools.  
- **Activity Bar**: Click the Source Control icon (shaped like a branch).  
- **Shortcut**: `Ctrl + Shift + G` (Windows/Linux) or `Cmd + Shift + G` (macOS)

### 4. View Commit History  
You can check the full commit history in a few ways:  
- Click the clock icon in the Source Control toolbar.  
- Or, right-click any file > **View Git History**.

### 5. Browse Commits  
In the Git History panel, you’ll see a list of commits showing the message, author, date, and hash. Click any commit to view details and code changes it introduced.

### 6. Compare Changes Between Commits  
To compare commits:  
- Hold `Ctrl` (or `Cmd` on macOS) and select two commits.  
- VS Code will open a side-by-side diff showing what changed.

### 7. View a File’s History  
To see how a specific file has changed over time:  
- **From Explorer**: Right-click the file > Git: View File History  
- **From Editor**: Right-click inside the file > Git: View File History

## 🔄 Tips for a Better Experience  
- **Use GitLens Extension**: Adds more detail like inline blame, commit annotations, and better file history navigation.  
- **Keyboard Shortcuts**:  
  - Open Source Control: `Ctrl + Shift + G` or `Cmd + Shift + G`  
  - Use arrow keys to move between commits  
  - Use the search bar to filter commits by author, date, or message  
- **Switch Branches** to view their individual commit logs in the Git History panel.

## ✅ Conclusion  
VS Code makes Git history browsing intuitive and efficient. With built-in features and helpful extensions, you can easily inspect changes, track progress, and understand your codebase better — all without leaving your editor.
