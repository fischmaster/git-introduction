# Git

Git is a free, open-source distributed version control system designed to handle projects of any size with speed and efficiency.

## What is Git?

Git is a tool that tracks changes in your files over time. It allows you to:

- Record the history of your project
- Revert to previous versions
- Work on multiple features simultaneously
- Collaborate with others

## Key Characteristics

### Distributed Version Control

Unlike centralized systems, Git gives every developer a full copy of the repository:

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ Developer A │     │ Developer B │     │ Developer C │
│ Full Repo   │     │ Full Repo   │     │ Full Repo   │
│ + History   │     │ + History   │     │ + History   │
└─────────────┘     └─────────────┘     └─────────────┘
       │                   │                   │
       └───────────────────┼───────────────────┘
                           │
                    ┌──────┴──────┐
                    │ Remote Repo │
                    │  (Optional) │
                    └─────────────┘
```

**Benefits:**
- Work offline with full functionality
- No single point of failure
- Faster operations (most are local)

### Snapshots, Not Differences

Git stores snapshots of your project, not just the differences:

```
Commit 1: [Snapshot A] ─── Full state of all files
Commit 2: [Snapshot B] ─── Full state of all files  
Commit 3: [Snapshot C] ─── Full state of all files
```

### Data Integrity

Every file and commit is checksummed using SHA-1 hashing:

```
Commit: a1b2c3d4e5f6...
```

This ensures:
- No data corruption goes undetected
- Every commit has a unique identifier
- History cannot be changed without detection

## Git vs Other Version Control Systems

| Feature | Git | SVN (Centralized) |
|---------|-----|-------------------|
| Repository | Full copy locally | Only working copy |
| Offline work | Full functionality | Limited |
| Branching | Fast and lightweight | Slow and heavy |
| Speed | Very fast | Slower |

## Core Concepts

| Concept | Description |
|---------|-------------|
| Repository | Storage for your project and its history |
| Commit | A snapshot of your project at a point in time |
| Branch | An independent line of development |
| Merge | Combining changes from different branches |
| Clone | Creating a copy of a repository |
| Push/Pull | Syncing with remote repositories |

## Brief History

- **2005**: Created by Linus Torvalds for Linux kernel development
- **Goal**: Speed, simple design, support for distributed development
- **Today**: Most widely used version control system in the world

## Installing Git

```bash
# macOS (with Homebrew)
brew install git

# Ubuntu/Debian
sudo apt-get install git

# Windows
# Download from https://git-scm.com/download/win
```

## Basic Configuration

```bash
# Set your identity
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check configuration
git config --list
```
