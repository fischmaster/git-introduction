# git checkout

Switch branches or restore working tree files.

## Usage

```bash
git checkout <branch-name>     # Switch to a branch
git checkout -b <new-branch>   # Create and switch to new branch
git checkout -- .              # Discard all local changes
git checkout -- <file>         # Discard changes in specific file
```

## Description

The `checkout` command serves two main purposes:
1. Switching between branches
2. Restoring files to a previous state

## Switching Branches

```bash
git checkout main              # Switch to main branch
git checkout feature-login     # Switch to feature branch
git checkout -b new-feature    # Create and switch in one step
```

## Discarding Changes

### Discard All Unstaged Changes
```bash
git checkout -- .
```
This restores all modified files in the working directory to their last committed state. **Warning:** This cannot be undone!

### Discard Changes in Specific File
```bash
git checkout -- filename.md
```

### Restore File from Specific Commit
```bash
git checkout abc123 -- filename.md
```

## Modern Alternative: git switch & git restore

Git 2.23+ introduced more intuitive commands:

```bash
# Switching branches (preferred)
git switch main
git switch -c new-branch       # Create and switch

# Restoring files (preferred)
git restore .                  # Discard all changes
git restore filename.md        # Discard specific file
```

## Important Notes

- Uncommitted changes may be lost when switching branches
- Use `git stash` to save changes temporarily before switching
