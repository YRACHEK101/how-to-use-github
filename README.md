# Git Commands Guide

This guide explains the basic Git commands for connecting to a GitHub repository and managing your code changes.

## Initial Setup

### 1. Configure Git
First-time setup on your computer:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 2. Initialize a Repository
Choose one of these methods:

#### Create a New Repository
```bash
# Create and enter your project folder
mkdir your-project
cd your-project

# Initialize Git
git init
```

#### Clone an Existing Repository
```bash
git clone https://github.com/username/repository-name.git
```

## Basic Workflow

### 1. Check Status
See which files have been changed:
```bash
git status
```

### 2. Add Files
```bash
# Add specific file
git add filename.ext

# Add multiple files
git add file1.ext file2.ext

# Add all changes
git add .
```

### 3. Commit Changes
```bash
# Commit with a message
git commit -m "Your descriptive commit message"

# Add and commit in one command (for tracked files only)
git commit -am "Your descriptive commit message"
```

### 4. Push Changes
```bash
# First time push
git push -u origin main

# Subsequent pushes
git push
```

## Working with Remotes

### Add Remote Repository
```bash
# Add a remote
git remote add origin https://github.com/username/repository-name.git

# View remote repositories
git remote -v
```

### Switch Branch
```bash
# Create and switch to a new branch
git checkout -b branch-name

# Switch to an existing branch
git checkout branch-name
```

## Common Commands

### View Changes
```bash
# See uncommitted changes
git diff

# See commit history
git log
```

### Undo Changes
```bash
# Undo changes in a file
git checkout filename.ext

# Reset staged changes
git reset filename.ext

# Reset all changes to last commit
git reset --hard
```

### Update Local Repository
```bash
# Fetch and merge changes
git pull

# Fetch changes without merging
git fetch
```

## Best Practices

1. **Commit Often**: Make small, focused commits
2. **Write Clear Messages**: Use descriptive commit messages
3. **Pull Before Push**: Always pull before pushing to avoid conflicts
4. **Use Branches**: Create branches for new features
5. **Review Changes**: Check `git status` and `git diff` before committing

## Handling Errors

### Fix Wrong Commit Message
```bash
# Fix last commit message
git commit --amend -m "New message"
```

### Undo Last Commit
```bash
# Undo commit but keep changes
git reset --soft HEAD~1

# Undo commit and discard changes
git reset --hard HEAD~1
```

## GitHub Authentication

### Using Personal Access Token
1. Go to GitHub Settings
2. Select Developer Settings
3. Generate Personal Access Token
4. Use token instead of password when pushing

### Using SSH
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Add SSH key to GitHub account
# Copy the public key (.pub file) to GitHub settings
```

## Need Help?

- View command help: `git help command`
- View command options: `git command -h`
- Check Git documentation: [Git Documentation](https://git-scm.com/doc)
- GitHub Guides: [GitHub Guides](https://guides.github.com)
