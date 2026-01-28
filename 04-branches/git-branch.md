# git branch

List, create, or delete branches.

## Usage

```bash
git branch                    # List local branches
git branch -a                 # List all branches (local + remote)
git branch <branch-name>      # Create a new branch
git branch -d <branch-name>   # Delete a branch (safe)
git branch -D <branch-name>   # Force delete a branch
```

## Description

Branches allow you to work on different features or fixes in isolation. The `git branch` command helps you manage these branches.

## Examples

### List Branches
```bash
git branch          # Shows local branches, current marked with *
git branch -a       # Shows all branches including remotes
git branch -v       # Shows branches with last commit info
```

### Create a Branch
```bash
git branch feature-login     # Creates branch but stays on current
git checkout -b feature-login  # Creates and switches to new branch
```

### Delete a Branch
```bash
git branch -d feature-login   # Delete if fully merged
git branch -D feature-login   # Force delete (unmerged changes lost)
```

### Rename a Branch
```bash
git branch -m old-name new-name   # Rename a branch
git branch -m new-name            # Rename current branch
```

## Branch Naming Conventions

- `feature/` - New features (e.g., `feature/user-auth`)
- `bugfix/` - Bug fixes (e.g., `bugfix/login-error`)
- `hotfix/` - Urgent fixes (e.g., `hotfix/security-patch`)
- `release/` - Release preparation (e.g., `release/v1.0`)
