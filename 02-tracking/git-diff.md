# git diff

Show changes between commits, commit and working tree, etc.

## Usage

```bash
git diff                  # Changes not yet staged
git diff --staged         # Changes staged for commit
git diff <commit1> <commit2>  # Changes between two commits
```

## Description

This command shows the differences between:
- Your working directory and the staging area (unstaged changes)
- The staging area and the last commit (staged changes)
- Any two commits or branches

## Example Output

```diff
diff --git a/file.md b/file.md
index 1234567..abcdefg 100644
--- a/file.md
+++ b/file.md
@@ -1,3 +1,4 @@
 # My File
 
 This is some content.
+This line was added.
```

Lines starting with `+` are additions, lines starting with `-` are deletions.
