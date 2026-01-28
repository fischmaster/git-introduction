# git merge

Join two or more development histories together.

## Usage

```bash
git merge <branch-name>           # Merge branch into current branch
git merge --no-ff <branch-name>   # Merge with a merge commit (no fast-forward)
git merge --abort                 # Abort a merge in progress
```

## Description

Merging integrates changes from one branch into another. Git will automatically combine the changes if possible, or flag conflicts for manual resolution.

## Merge Types

### Fast-Forward Merge (Default)
When the current branch has no new commits since the branch was created:
```bash
git checkout main
git merge feature-branch
```
Result: Linear history, no merge commit created.

### No Fast-Forward Merge
Forces creation of a merge commit even when fast-forward is possible:
```bash
git checkout main
git merge --no-ff feature-branch
```
Result: Preserves branch history with explicit merge commit.

## When to Use --no-ff

Use `--no-ff` when you want to:
- Preserve the context of a feature branch
- Make it clear where a feature was integrated
- Maintain a cleaner history for reverting features

## Handling Merge Conflicts

When Git can't automatically merge:

1. Git marks the conflicted files
2. Open conflicted files and look for conflict markers:
   ```
   <<<<<<< HEAD
   Your changes
   =======
   Their changes
   >>>>>>> feature-branch
   ```
3. Resolve by editing the file
4. Stage the resolved file: `git add <file>`
5. Complete the merge: `git commit`

## Abort a Merge
```bash
git merge --abort    # Cancel merge and restore previous state
```
