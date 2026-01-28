# Git Introduction

A hands-on introduction to Git version control and GitHub.

## Repository Structure

This repository contains documentation and examples organized by Git workflow:

```
git-introduction/
├── 01-setup/          # Repository initialization
├── 02-tracking/       # Tracking changes
├── 03-commits/        # Committing and history
├── 04-branches/       # Branching and merging
├── 05-remote/         # Remote collaboration
└── README.md          # This file
```

## Quick Command Reference

### Setup
| Command | Description |
|---------|-------------|
| `git init` | Initialize a new repository |
| `git clone <url>` | Clone an existing repository |

### Tracking Changes
| Command | Description |
|---------|-------------|
| `git status` | Show working tree status |
| `git diff` | Show changes not yet staged |
| `git add <file>` | Stage a file for commit |
| `git add .` | Stage all changes |

### Commits & History
| Command | Description |
|---------|-------------|
| `git commit -m "message"` | Commit staged changes |
| `git log` | Show commit history |
| `git log --stat` | Show commit history with stats |
| `git log --pretty=oneline` | Compact log format |
| `git log --pretty=format:"%h %s" --graph` | Custom format with graph |

### Branches
| Command | Description |
|---------|-------------|
| `git branch` | List branches |
| `git branch <name>` | Create a new branch |
| `git checkout <branch>` | Switch to a branch |
| `git checkout -- .` | Discard all local changes |

### Merging
| Command | Description |
|---------|-------------|
| `git merge <branch>` | Merge branch into current |
| `git merge --no-ff <branch>` | Merge with merge commit |

### Remote Operations
| Command | Description |
|---------|-------------|
| `git push` | Push commits to remote |
| `git push origin <branch>` | Push specific branch |
| `git pull origin <branch>` | Pull changes from remote |

## Getting Started

1. Navigate to the `01-setup/` folder to learn about initializing repositories
2. Follow the numbered folders in sequence for a logical learning path
3. Each markdown file contains explanations and examples

## License

This project is for educational purposes.
