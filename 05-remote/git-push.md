# git push

Upload local commits to a remote repository.

## Usage

```bash
git push                          # Push to tracked remote branch
git push origin <branch-name>     # Push specific branch to origin
git push -u origin <branch-name>  # Push and set upstream tracking
git push origin --all             # Push all branches
```

## Description

The `push` command uploads your local commits to a remote repository (like GitHub). This shares your work with others and backs up your code.

## Common Scenarios

### Push to Current Branch
```bash
git push
```
Works when your branch is already tracking a remote branch.

### Push to Specific Remote and Branch
```bash
git push origin main
git push origin feature-branch
```
Explicitly specify the remote (`origin`) and branch name.

### Set Upstream and Push
```bash
git push -u origin feature-branch
```
The `-u` flag sets up tracking, so future `git push` commands work without arguments.

## Push a New Branch

When you create a local branch and want to push it for the first time:
```bash
git checkout -b new-feature
# ... make commits ...
git push -u origin new-feature
```

## Common Options

- `-u` / `--set-upstream` : Set remote tracking branch
- `--force` / `-f` : Force push (overwrites remote) - **use with caution!**
- `--tags` : Push all tags
- `--delete` : Delete a remote branch

## Delete Remote Branch
```bash
git push origin --delete old-branch
```

## Important Notes

- Always `git pull` before pushing to avoid conflicts
- Never force push to shared branches (like `main`)
- Use `git push --force-with-lease` for safer force pushes
