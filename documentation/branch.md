# Branch

A branch is an independent line of development that allows you to work on features, fixes, or experiments in isolation from the main codebase.

## What is a Branch?

Think of a branch as a parallel universe for your code. When you create a branch, you're creating a copy of your project at that point in time where you can make changes without affecting the original.

```
main:     A───B───C───D───E
                   \
feature:            F───G───H
```

In this diagram:
- `main` continues development with commits D and E
- `feature` branch diverges at C and has its own commits F, G, H
- Both branches exist independently

## Why Use Branches?

1. **Isolation**: Work on new features without breaking working code
2. **Parallel Development**: Multiple people can work on different features simultaneously
3. **Experimentation**: Try new ideas safely; delete the branch if it doesn't work
4. **Organization**: Keep different types of work separate

## The Main Branch

Every repository has a default branch, typically called `main` (or `master` in older repositories). This branch usually contains:

- Production-ready code
- Stable, tested features
- The "official" version of the project

## Branch Lifecycle

```
1. Create       2. Develop      3. Merge        4. Delete
   branch          on branch       to main         branch

     ┌──●──●──┐
main ●─────────●───────●
     create   commits  merge
```

### 1. Create a Branch
```bash
git branch feature-login      # Create branch
git checkout feature-login    # Switch to it
# Or in one command:
git checkout -b feature-login
```

### 2. Work on the Branch
```bash
# Make changes, then:
git add .
git commit -m "Add login form"
```

### 3. Merge Back
```bash
git checkout main             # Switch to main
git merge feature-login       # Merge feature into main
```

### 4. Delete the Branch
```bash
git branch -d feature-login   # Delete after merging
```

## Local vs Remote Branches

| Type | Location | Example |
|------|----------|---------|
| Local | Your computer | `feature-login` |
| Remote | Server (GitHub) | `origin/feature-login` |
| Tracking | Local linked to remote | `feature-login` → `origin/feature-login` |

```bash
# View local branches
git branch

# View remote branches
git branch -r

# View all branches
git branch -a
```

## Branch Naming Conventions

Good branch names are descriptive and follow a pattern:

| Prefix | Purpose | Example |
|--------|---------|---------|
| `feature/` | New functionality | `feature/user-authentication` |
| `bugfix/` | Bug repairs | `bugfix/login-redirect` |
| `hotfix/` | Urgent production fixes | `hotfix/security-patch` |
| `release/` | Release preparation | `release/v2.0.0` |
| `docs/` | Documentation updates | `docs/api-reference` |
