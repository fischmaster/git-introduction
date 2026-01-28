# git log

Show commit history.

## Usage

```bash
git log                           # Full log output
git log --oneline                 # Compact one-line format
git log --stat                    # Show file change statistics
git log --pretty=oneline          # One line per commit
git log --pretty=format:"%h %s" --graph  # Custom format with graph
```

## Description

This command shows the commit history for the current branch. It displays commits in reverse chronological order (newest first).

## Common Options

### Basic Options
```bash
git log -n 5          # Show only last 5 commits
git log --oneline     # Abbreviated output
git log --stat        # Show files changed and insertions/deletions
```

### Pretty Formats
```bash
git log --pretty=oneline              # Hash and message on one line
git log --pretty=format:"%h %s"       # Short hash and subject
git log --pretty=format:"%h - %an: %s" # Hash, author, subject
```

### Visual Graph
```bash
git log --graph                       # ASCII graph of branches
git log --pretty=format:"%h %s" --graph  # Graph with custom format
git log --oneline --graph --all       # Graph of all branches
```

## Format Placeholders

- `%h` - Abbreviated commit hash
- `%s` - Subject (commit message)
- `%an` - Author name
- `%ar` - Author date, relative
- `%d` - Ref names (branches, tags)

## Example Output

```
* a1b2c3d Add new feature
* e4f5g6h Fix bug in login
* i7j8k9l Initial commit
```
