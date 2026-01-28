# git clone

Clone an existing repository from a remote location.

## Usage

```bash
git clone <repository-url>
git clone <repository-url> <directory-name>
```

## Description

This command creates a copy of an existing Git repository. It automatically:
- Creates a new directory
- Initializes a `.git` directory inside it
- Pulls down all the data from the repository
- Checks out a working copy of the latest version

## Example

```bash
git clone https://github.com/username/repository.git
git clone https://github.com/username/repository.git my-local-folder
```

The second example clones the repository into a folder named `my-local-folder` instead of the default repository name.
