# 03 — Undoing Mistakes

## Unstage a File

```bash
git restore --staged file.txt    # Unstage (keep changes)
git restore file.txt            # Discard working changes (DANGER!)
```

## Amend Last Commit

```bash
git commit --amend -m "better message"  # Change last commit message
# Or add forgotten files:
git add forgotten_file.txt
git commit --amend                  # Add to last commit
```

## Revert a Commit (Safe)

```bash
git revert <commit-hash>    # Creates new commit that undoes the old one
# Safe because it doesn't rewrite history
```

## Reset (Dangerous — Rewrites History)

```bash
git reset --soft HEAD~1    # Undo commit, keep changes staged
git reset --mixed HEAD~1   # Undo commit, keep changes unstaged (default)
git reset --hard HEAD~1    # Undo commit, DISCARD changes (DANGER!)
```

## Reset vs Revert

| Feature | Reset | Revert |
|---------|-------|--------|
| Rewrites history | Yes | No |
| Safe for shared | No | Yes |
| Creates new commit | No | Yes |
| Use case | Local fixes | Shared repos |

## Recover Lost Commits

```bash
git reflog              # Shows ALL commit history including lost ones
git reset --hard <hash> # Restore to any point
```

## Checkout Old Version

```bash
git checkout <hash> -- file.txt    # Restore specific file from old commit
```

## Interactive Rebase

```bash
git rebase -i HEAD~5    # Edit last 5 commits
```

Options: pick, squash (merge into previous), drop (delete), reword (change message).

## Practice

1. Last commit ka message change karo (`--amend`).
2. 3 commits pe `git reset --soft` try karo aur samjho difference.
3. `git reflog` use karke ek "lost" commit recover karo.

---
*Next: 04-github-collaboration.md →*


## Quick Tip

Practice makes perfect. Don't just read — write code!


## Resources

- [Official Docs](https://docs.example.com)
- [Tutorial](https://tutorial.example.com)


---

> Note: Reviewed this section, looks good.
