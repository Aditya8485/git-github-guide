# 01 — Git Basics

## What is Git?

Git is a version control system. Har change ka record rakhta hai — 
wapas ja sakte hain, branches bana sakte hain, team ke saath collaborate kar sakte hain.

## Init & First Commit

```bash
git init                    # Initialize repo
git add .                   # Stage all files
git add file.txt           # Stage specific file
git commit -m "first commit" # Commit with message
git status                  # Check status
git log                     # View history
```

## Workflow

```
Working Directory → (git add) → Staging Area → (git commit) → Repository
```

## Connecting to GitHub

```bash
git remote add origin https://github.com/user/repo.git
git push -u origin main
git pull origin main
git clone https://github.com/user/repo.git
```

## Common Commands

```bash
git status              # what changed?
git diff                # see changes (unstaged)
git diff --staged       # see changes (staged)
git log --oneline       # compact log
git log --oneline --graph --all  # visual branch history
git show <hash>        # see specific commit
```

## .gitignore

Ignore files jo track nahi karne:

```
node_modules/
.env
*.log
__pycache__/
.DS_Store
```

## Practice

1. Ek naya repo banao, kuch files add karo, commit karo, GitHub pe push karo.
2. `.gitignore` banao — node_modules, .env, log files ignore karo.
3. `git log --oneline --graph` run karo aur history samjho.

---
*Next: 02-branching-merging.md →*


<!-- TODO: add more examples here -->


## Additional Note

Added some more thoughts on this topic.


## Additional Note

Added some more thoughts on this topic.
