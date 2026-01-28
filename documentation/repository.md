# Repository

A repository (often called "repo") is a storage location for your project that contains all of your project's files and the entire revision history.

## What is a Repository?

A Git repository tracks and saves the history of all changes made to the files in a project. It contains:

- All project files and folders
- The complete history of changes (commits)
- Branch information
- Configuration settings

Think of it as a database of your project's evolution over time.

## Local vs Remote Repository

### Local Repository

A **local repository** exists on your personal computer. It's where you do your actual work.

```
Your Computer
└── my-project/
    ├── .git/          ← Local repository (hidden folder)
    ├── src/
    ├── docs/
    └── README.md
```

**Characteristics:**
- Stored on your machine
- Only you have access (unless you share your computer)
- You can work offline
- Contains the full project history
- Created with `git init` or `git clone`

### Remote Repository

A **remote repository** is hosted on a server (like GitHub, GitLab, or Bitbucket). It serves as a central hub for collaboration.

```
GitHub/GitLab/Bitbucket
└── username/my-project.git   ← Remote repository
```

**Characteristics:**
- Stored on a server/cloud
- Accessible by team members
- Requires internet connection to sync
- Acts as a backup
- Enables collaboration

## How Local and Remote Work Together

```
┌─────────────────┐                    ┌─────────────────┐
│  Local Repo     │    git push →      │  Remote Repo    │
│  (Your PC)      │    ← git pull      │  (GitHub)       │
└─────────────────┘                    └─────────────────┘
```

| Action | Command | Direction |
|--------|---------|-----------|
| Upload changes | `git push` | Local → Remote |
| Download changes | `git pull` | Remote → Local |
| Copy repository | `git clone` | Remote → Local |
| Link repositories | `git remote add` | Establishes connection |

## Common Remote Operations

```bash
# View configured remotes
git remote -v

# Add a remote repository
git remote add origin https://github.com/user/repo.git

# Push to remote
git push origin main

# Pull from remote
git pull origin main
```

## Why Use Both?

1. **Backup**: Remote serves as a backup if your local machine fails
2. **Collaboration**: Team members can push and pull changes
3. **Deployment**: Remote can trigger deployments
4. **Code Review**: Remote platforms offer pull request features
5. **Offline Work**: Local allows you to work without internet
