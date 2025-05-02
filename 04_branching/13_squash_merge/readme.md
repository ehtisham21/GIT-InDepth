## Squash Merges in Git
### Table of Contents
- [Introduction](#introduction)
- [What is a Squash Merge?](#what-is-a-squash-merge)
- [When to Use Squash Merges](#when-to-use-squash-merges)
- [Example Demonstration](#example-demonstration)
1. [Initialize a Git Repository](#initialize-a-git-repository)
2. [Create a Main Branch and Make an Initial Commit](#create-a-main-branch-and-make-an-initial-commit)
3. [Create a Feature Branch and Make Multiple Commits](#create-a-feature-branch-and-make-multiple-commits)
4. [Perform a Squash Merge into Main Branch](#perform-a-squash-merge-into-main-branch)
5. [View Commit History After Squash Merge](#view-commit-history-after-squash-merge)
- [Summary](#summary)
- [Additional Tips](#additional-tips)

### Introduction
Squash merges in Git help maintain a clean and understandable project timeline by consolidating multiple commits from a feature branch into a single commit on the target branch.

### What is a Squash Merge?
A squash merge condenses all individual commits from the source branch into a single commit on the target branch, keeping the commit history clean and focused.

### When to Use Squash Merges
- **Feature Completion**: Combine small commits representing incremental progress into a single commit.
- **Bug Fixes**: Squash multiple commits addressing different aspects of a single bug for clarity.
- **Code Cleanup**: Combine commits involving code formatting, documentation updates, or minor tweaks.

### Example Demonstration

#### Initialize a Git Repository
```bash
mkdir git-squash-merge-demo
cd git-squash-merge-demo
git init
```
Initialized empty Git repository in /path/to/git-squash-merge-demo/.git/

#### Create a Main Branch and Make an Initial Commit
```bash
echo "Initial content" > file.txt
git add file.txt
git commit -m "Initial commit"
```
[master (root-commit) ca49180] Initial commit
1 file changed,1 insertion(+)
 create mode100644 file.txt

#### Create a Feature Branch and Make Multiple Commits
```bash
git checkout -b feature
echo "Feature work1" >> file.txt
git add file.txt
git commit -m "Add feature work1"

echo "Feature work2" >> file.txt
git add file.txt
git commit -m "Add feature work2"
```
Switched to a new branch 'feature'
[feature49a023f] Add feature work1
1 file changed,1 insertion(+)
[feature d0e95c0] Add feature work2
1 file changed,1 insertion(+)

#### Perform a Squash Merge into Main Branch
```bash
git checkout main
git merge --squash feature
git commit -m "Squash merge feature branch"
```
On branch main
All conflicts fixed but you are still merging.
 (use "git commit" to conclude merge)

Changes to be committed:
 modified: file.txt

[main84d855e] Squash merge feature branch
1 file changed,2 insertions(+)

#### View Commit History After Squash Merge
```bash
git log --oneline --graph
```
*84d855e (HEAD -> main) Squash merge feature branch
|\
| * d0e95c0 (feature) Add feature work2
| *49a023f Add feature work1
|/
* ca49180 Initial commit

### Summary

| Command | Description | Example Output |
| --- | --- | --- |
| `git checkout -b feature` | Creates and switches to a new branch named feature | Switched to a new branch 'feature' |
| `git commit -m "Add feature work1"` | Commits staged changes with the message "Add feature work1" | [feature49a023f] Add feature work1 |
| `git merge --squash feature` | Merges changes from feature into main by squashing commits | Prepares the merge; no immediate output |
| `git commit -m "Squash merge feature branch"` | Creates a single commit on main that includes all changes from feature | [main84d855e] Squash merge feature branch |
| `git log --oneline --graph` | Displays the commit history with a graphical representation | Commit graph with squash merge |

### Additional Tips
- **Interactive Rebase Before Merging**: Use `git rebase -i` to clean up your feature branch's commit history.
- **Use Descriptive Commit Messages**: Craft a meaningful commit message that encapsulates all changes from the feature branch.
- **Leverage Git Extensions**: Use GitLens for enhanced Git visualization and management features.
- **Automate Merge Strategies**: Configure Git to use squash merges by default for specific branches or workflows.
- **Backup Branches Before Merging**: Create backup branches to safeguard against unintended changes during merges.
- **Clean Up Feature Branches After Merge**: Delete feature branches after they've been successfully merged.