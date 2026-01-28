# git status

Show the working tree status.

## Usage

```bash
git status
```

## Description

This command displays the state of the working directory and the staging area. It shows:
- Which changes have been staged
- Which changes have not been staged
- Which files are not being tracked by Git

## Example Output

```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   file1.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
        modified:   file2.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        newfile.md
```

Use `git status` frequently to understand what state your files are in.
