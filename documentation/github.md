# GitHub

GitHub is a web-based platform that hosts Git repositories and provides collaboration tools for software development.

## What is GitHub?

GitHub is a cloud service built on top of Git that adds:

- Remote repository hosting
- Collaboration features
- Project management tools
- Social coding features

Think of it as social media for code—you can share, collaborate, and contribute to projects worldwide.

## Git vs GitHub

| Git | GitHub |
|-----|--------|
| Version control software | Hosting platform |
| Runs locally on your computer | Runs in the cloud |
| Command-line tool | Web interface + API |
| Free and open-source | Free tier + paid plans |
| Created by Linus Torvalds | Created by GitHub, Inc. (now Microsoft) |

```
┌─────────────────┐                  ┌─────────────────┐
│      Git        │                  │     GitHub      │
│   (The Tool)    │  ◄── pushes ──►  │  (The Platform) │
│                 │  ◄── pulls ───►  │                 │
│ Local computer  │                  │ Cloud hosting   │
└─────────────────┘                  └─────────────────┘
```

**Key Point:** You can use Git without GitHub, but GitHub requires Git.

## Core GitHub Features

### 1. Repository Hosting

Store your Git repositories in the cloud:

```
https://github.com/username/repository-name
```

- Public repositories (visible to everyone)
- Private repositories (restricted access)
- Unlimited repositories on free tier

### 2. Pull Requests

A way to propose changes and request code review:

```
1. Fork or branch the repository
2. Make your changes
3. Open a Pull Request
4. Team reviews and discusses
5. Merge when approved
```

### 3. Issues

Track bugs, features, and tasks:

- Create issue tickets
- Assign to team members
- Add labels and milestones
- Link to pull requests

### 4. Actions (CI/CD)

Automate workflows:

```yaml
# Example: Run tests on every push
name: Tests
on: [push]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: npm test
```

### 5. GitHub Pages

Host static websites directly from a repository:

```
https://username.github.io/repository-name
```

## GitHub Workflow

```
┌──────────────────────────────────────────────────────────────┐
│                      GitHub Workflow                          │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  1. Clone         2. Branch        3. Commit & Push          │
│  ─────────        ─────────        ────────────────          │
│  git clone ...    git checkout     git add .                 │
│                   -b feature       git commit -m "..."       │
│                                    git push                  │
│                                                              │
│  4. Pull Request  5. Review        6. Merge                  │
│  ──────────────   ─────────        ─────────                 │
│  Open PR on       Team reviews     Merge to main             │
│  GitHub           code & comments  Delete branch             │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

## GitHub Alternatives

Other platforms that host Git repositories:

| Platform | Key Feature |
|----------|-------------|
| GitLab | Self-hosted option, built-in CI/CD |
| Bitbucket | Atlassian integration (Jira, Trello) |
| Azure DevOps | Microsoft ecosystem integration |
| Gitea | Lightweight, self-hosted |

## Getting Started with GitHub

1. **Create an account** at [github.com](https://github.com)

2. **Create a new repository** on GitHub

3. **Connect local repo to GitHub**:
   ```bash
   git remote add origin https://github.com/username/repo.git
   git push -u origin main
   ```

4. **Or clone an existing repo**:
   ```bash
   git clone https://github.com/username/repo.git
   ```

## Authentication

GitHub requires authentication for pushing code:

### HTTPS (with Personal Access Token)
```bash
git clone https://github.com/username/repo.git
# Enter username and token when prompted
```

### SSH (recommended)
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Add to GitHub account (Settings → SSH Keys)

# Clone with SSH
git clone git@github.com:username/repo.git
```

## Why Use GitHub?

1. **Backup**: Your code is safely stored in the cloud
2. **Collaboration**: Work with teammates easily
3. **Visibility**: Showcase your work (portfolio)
4. **Community**: Contribute to open-source projects
5. **Integration**: Connect with other tools and services
