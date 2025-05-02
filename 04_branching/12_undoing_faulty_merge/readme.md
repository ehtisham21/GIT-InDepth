## Undoing a Faulty Merge in Git
### Table of Contents
- [Introduction](#introduction)
- [Example Demonstration](#example-demonstration)
  1. [View Commit History](#view-commit-history)
  2. [Reset to Previous Commit](#reset-to-previous-commit)
  3. [Reset to a Specific Commit](#reset-to-a-specific-commit)
  4. [Attempt to Revert the Merge Commit](#attempt-to-revert-the-merge-commit)
  5. [Revert the Merge Commit with Parent Specification](#revert-the-merge-commit-with-parent-specification)
- [Summary](#summary)
- [Additional Tips](#additional-tips)

### Introduction
In software development, faulty merges can disrupt your workflow. A faulty merge introduces unintended changes or conflicts, complicating project history. Knowing how to undo a faulty merge ensures your repository remains clean and your project history understandable.

### Example Demonstration
Let's explore how to undo a faulty merge using Git commands.

#### View Commit History
```bash
git log --oneline --all --graph
```
Displays commit history in a concise, graphical format.

#### Reset to Previous Commit
```bash
git reset --hard HEAD~1
```
Resets the repository to the state before the last commit, discarding changes.

#### Reset to a Specific Commit
```bash
git reset --hard <commit-hash>
```
Resets the repository to a specified commit, discarding changes.

#### Attempt to Revert the Merge Commit
```bash
git revert HEAD
```
Attempts to revert the last commit but fails if it's a merge commit without specifying a parent.

#### Revert the Merge Commit with Parent Specification
```bash
git revert -m1 HEAD
```
Reverts the last merge commit by specifying the first parent branch.

### Summary

| Command | Description | Example Output |
| --- | --- | --- |
| `git log --oneline --all --graph` | Displays commit history | Commit graph |
| `git reset --hard HEAD~1` | Resets to previous commit | HEAD is now at ad4f937 |
| `git reset --hard <commit-hash>` | Resets to a specific commit | HEAD is now at ad4f937 |
| `git revert HEAD` | Attempts to revert last commit | error: commit <hash> is a merge |
| `git revert -m1 HEAD` | Reverts merge commit | [master56ea239] Revert "Merge branch 'bugfix'" |

### Additional Tips
- **Create Backup Branches**: Before risky operations, create a backup branch.
- **Use Tags**: Tag important commits for easy reference.
- **Leverage Git Extensions**: Use GitLens for enhanced visualization and management.
- **Understand Git Reflog**: Track updates to branch tips and recover lost commits.
- **Practice Safe Merging**: Regularly pull changes and communicate with your team.