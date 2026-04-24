# 02 — Branching & Merging

## Branches

Branch = parallel timeline. Main code safe rahta hai, experiments alag branch pe.

```bash
git branch                   # List branches
git branch feature-login     # Create branch
git checkout feature-login    # Switch to branch
git checkout -b feature-x    # Create + switch in one command
git switch main              # Switch to main (newer way)
```

## Merge

```bash
# On main branch
git checkout main
git merge feature-login       # Merge feature into main
git branch -d feature-login  # Delete merged branch
```

## Merge Conflicts

Jab dono branches mein same file ko alag alag modify kiya ho:

```
<<<<<<< HEAD
code from current branch
=======
code from incoming branch
>>>>>>> feature-branch
```

Resolve manually → stage → commit.

## Rebase (Alternative to Merge)

```bash
git checkout feature
git rebase main
```

Linear history — looks cleaner. But: don't rebase shared branches!

Merge vs Rebase:
- Merge: preserves history, creates merge commit
- Rebase: rewrites history, cleaner but dangerous on shared branches

## Common Workflow: Feature Branch

```bash
git checkout -b feature/new-button   # Create feature branch
# ... make changes, commit ...
git checkout main                       # Switch to main
git pull origin main                   # Update main
git merge feature/new-button           # Merge feature
git push origin main                   # Push
git branch -d feature/new-button       # Clean up
```

## Stash

```bash
git stash               # Save uncommitted work
git stash pop           # Restore and remove from stash
git stash list          # List stashes
git stash apply         # Restore without removing
```

## Practice

1. `main` branch pe 2 feature branches banao, alag alag changes karo, merge karo.
2. Conflict create karo aur resolve karo manually.
3. Stash use karke work save karo, branch switch karo, wapas aao.

---
*Next: 03-undoing-mistakes.md →*
