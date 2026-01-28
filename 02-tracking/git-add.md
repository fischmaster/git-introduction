# git add

Add file contents to the staging area (index).

## Usage

```bash
git add <file>           # Add a specific file
git add <directory>      # Add all files in a directory
git add .                # Add all changes in current directory
git add -A               # Add all changes in the repository
```

## Description

This command adds changes to the staging area, preparing them for the next commit. The staging area is like a preparation zone where you can review and organize your changes before committing.

## Examples

```bash
# Add a single file
git add readme.md

# Add multiple specific files
git add file1.md file2.md

# Add all changes (new, modified, deleted)
git add .
```

## Staging Workflow

1. Make changes to files
2. Use `git status` to see what changed
3. Use `git add` to stage specific changes
4. Use `git commit` to save staged changes

Remember: `git add .` stages everything in the current directory and subdirectories.
