# git commit

Record changes to the repository.

## Usage

```bash
git commit -m "Your commit message"
git commit -m "Short summary" -m "Longer description"
git commit                    # Opens editor for message
```

## Description

This command takes all staged changes and creates a new commit in the repository history. Each commit is a snapshot of your project at a specific point in time.

## Best Practices for Commit Messages

- Use present tense: "Add feature" not "Added feature"
- Keep the first line under 50 characters
- Be descriptive but concise
- Reference issue numbers if applicable

## Examples

```bash
# Simple commit with message
git commit -m "Add user authentication feature"

# Commit with title and body
git commit -m "Fix login bug" -m "Users were unable to log in when using special characters in passwords."

# Stage and commit all tracked files in one step
git commit -am "Update documentation"
```

## Common Options

- `-m` : Specify the commit message inline
- `-a` : Automatically stage all modified tracked files
- `--amend` : Modify the most recent commit
