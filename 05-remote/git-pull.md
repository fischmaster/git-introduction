# git pull

Fetch and integrate changes from a remote repository.

## Usage

```bash
git pull                          # Pull from tracked remote branch
git pull origin <branch-name>     # Pull specific branch from origin
git pull --rebase                 # Pull and rebase instead of merge
```

## Description

The `pull` command fetches changes from a remote repository and immediately merges them into your current branch. It's essentially `git fetch` + `git merge` in one command.

## Common Scenarios

### Pull from Tracked Branch
```bash
git pull
```
Downloads and merges changes from the remote branch your local branch is tracking.

### Pull from Specific Remote and Branch
```bash
git pull origin main
git pull origin develop
```
Explicitly fetches and merges from the specified remote and branch.

## Pull vs Fetch

| Command | What it does |
|---------|--------------|
| `git fetch` | Downloads changes but doesn't merge |
| `git pull` | Downloads AND merges changes |

```bash
# These are equivalent:
git pull origin main

# Same as:
git fetch origin main
git merge origin/main
```

## Pull with Rebase

Instead of creating a merge commit, rebase puts your commits on top:
```bash
git pull --rebase origin main
```

Benefits of rebasing:
- Cleaner, linear history
- Easier to read commit log
- Avoids unnecessary merge commits

## Handling Pull Conflicts

If your local changes conflict with remote changes:

1. Git will pause and mark conflicts
2. Resolve conflicts in affected files
3. Stage resolved files: `git add <file>`
4. Complete the merge: `git commit`

Or abort and try again:
```bash
git merge --abort
```

## Best Practices

- Pull frequently to stay up to date
- Commit or stash local changes before pulling
- Use `git pull --rebase` for feature branches
