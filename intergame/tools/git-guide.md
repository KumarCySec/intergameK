# Git Mastery Guide 🗂️

## Overview

This guide covers all Git operations used in the Interactive Coding Challenges, from basic commands to advanced techniques.

## 🔧 Basic Commands

### Repository Management

```bash
# Clone a repository
git clone <repository-url>

# Initialize a new repository
git init

# Check repository status
git status

# View commit history
git log
git log --oneline
git log --graph --oneline --all
```

### File Operations

```bash
# Add files to staging
git add <filename>
git add .  # Add all files

# Commit changes
git commit -m "Your commit message"
git commit -am "Add and commit tracked files"

# Remove files
git rm <filename>
git rm --cached <filename>  # Remove from tracking but keep file
```

## 🌿 Branching Operations

### Branch Management

```bash
# List branches
git branch
git branch -a  # All branches (local and remote)

# Create and switch to new branch
git checkout -b <branch-name>
git switch -c <branch-name>  # Modern syntax

# Switch between branches
git checkout <branch-name>
git switch <branch-name>

# Delete branch
git branch -d <branch-name>  # Safe delete
git branch -D <branch-name>  # Force delete
```

### Merging

```bash
# Merge branch into current branch
git merge <branch-name>

# Merge with no fast-forward
git merge --no-ff <branch-name>

# Abort merge if conflicts
git merge --abort
```

## 🔍 Advanced Git Operations

### Git Blame

```bash
# See who changed each line
git blame <filename>

# Blame with line numbers
git blame -L 10,20 <filename>

# Blame with commit info
git blame -w <filename>  # Ignore whitespace changes
```

### Git Bisect

```bash
# Start bisect process
git bisect start

# Mark current commit as bad
git bisect bad

# Mark a known good commit
git bisect good <commit-hash>

# Git will checkout a commit for testing
# After testing, mark as good or bad
git bisect good
git bisect bad

# Reset bisect when done
git bisect reset
```

### Git Stash

```bash
# Stash current changes
git stash
git stash push -m "Stash message"

# List stashes
git stash list

# Apply stash
git stash apply  # Keep stash
git stash pop    # Apply and remove stash

# Show stash contents
git stash show
git stash show -p  # Show patch

# Drop stash
git stash drop
git stash clear   # Remove all stashes
```

### Git Cherry-Pick

```bash
# Apply specific commit to current branch
git cherry-pick <commit-hash>

# Cherry-pick without auto-commit
git cherry-pick --no-commit <commit-hash>

# Cherry-pick range
git cherry-pick <start-commit>..<end-commit>
```

## 🔄 Remote Operations

### Remote Management

```bash
# List remotes
git remote -v

# Add remote
git remote add <name> <url>

# Remove remote
git remote remove <name>

# Change remote URL
git remote set-url <name> <new-url>
```

### Fetch and Pull

```bash
# Fetch from remote
git fetch <remote-name>
git fetch --all

# Pull changes
git pull <remote> <branch>
git pull --rebase  # Rebase instead of merge
```

### Push Operations

```bash
# Push to remote
git push <remote> <branch>
git push -u origin <branch>  # Set upstream

# Force push (use with caution)
git push --force-with-lease
```

## 🏷️ Tags and References

### Tag Management

```bash
# Create lightweight tag
git tag <tag-name>

# Create annotated tag
git tag -a <tag-name> -m "Tag message"

# List tags
git tag
git tag -l "v1.*"  # Pattern matching

# Push tags
git push origin <tag-name>
git push origin --tags  # Push all tags

# Delete tag
git tag -d <tag-name>
git push origin --delete <tag-name>
```

## 🔍 Investigation Commands

### Git Log Variations

```bash
# Show commits by author
git log --author="Author Name"

# Show commits affecting specific file
git log --follow <filename>

# Show commits with patches
git log -p

# Show commits with stats
git log --stat

# Show commits in graph format
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'
```

### Git Show

```bash
# Show commit details
git show <commit-hash>

# Show file at specific commit
git show <commit-hash>:<filename>

# Show differences
git show <commit-hash>
```

### Git Diff

```bash
# Show unstaged changes
git diff

# Show staged changes
git diff --cached

# Show changes between commits
git diff <commit1> <commit2>

# Show changes in specific file
git diff <commit1> <commit2> <filename>
```

## 🛠️ Configuration

### User Configuration

```bash
# Set user name and email
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Set default editor
git config --global core.editor "vim"

# Set default branch name
git config --global init.defaultBranch main
```

### Aliases

```bash
# Create useful aliases
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.unstage 'reset HEAD --'
```

## 🚨 Troubleshooting

### Reset Operations

```bash
# Soft reset (keep changes staged)
git reset --soft <commit-hash>

# Mixed reset (keep changes unstaged)
git reset --mixed <commit-hash>

# Hard reset (discard all changes)
git reset --hard <commit-hash>

# Reset to remote
git reset --hard origin/main
```

### Reflog

```bash
# View reflog (recent actions)
git reflog

# Reset to reflog entry
git reset --hard HEAD@{n}
```

### Clean

```bash
# Remove untracked files
git clean -f

# Remove untracked files and directories
git clean -fd

# Dry run (see what would be removed)
git clean -n
```

## 📚 Challenge-Specific Commands

### For Repository Dungeon Escape

```bash
# Switch branches
git checkout <branch-name>

# View commit history
git log --oneline

# Search commit messages
git log --grep="puzzle"
```

### For Code Heist

```bash
# Find who changed specific lines
git blame <filename>

# Binary search for bug
git bisect start
git bisect bad
git bisect good <commit-hash>
```

### For Stash Treasure Hunt

```bash
# List stashes
git stash list

# Show stash contents
git stash show -p stash@{n}

# Apply specific stash
git stash apply stash@{n}
```

---

**Master these commands and you'll be ready for any Git challenge! 🚀**
