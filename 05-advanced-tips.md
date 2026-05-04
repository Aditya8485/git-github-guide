# 05 — Advanced Git Tips

## Git Aliases

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.lg "log --oneline --graph --all"
```

Now: `git co main`, `git st`, `git lg`

## Cherry Pick

```bash
git cherry-pick <commit-hash>    # Apply specific commit to current branch
```

## Bisect (Find Bug-Introducing Commit)

```bash
git bisect start
git bisect bad          # Current commit has bug
git bisect good <hash>  # This commit was good
# Git will checkout commits one by one — mark good/bad
git bisect reset        # Done
```

## Git Hooks

```bash
# .git/hooks/pre-commit
#!/bin/bash
echo "Running tests..."
npm test
if [ $? -ne 0 ]; then
    echo "Tests failed! Commit blocked."
    exit 1
fi
```

## Submodules

```bash
git submodule add https://github.com/user/library.git libs/library
git submodule update --init --recursive
```

## Worktrees

```bash
git worktree add ../feature-login feature/login
# Work on 2 branches simultaneously in different folders!
```

## Clean Up

```bash
git clean -fd            # Remove untracked files and directories
git prune                # Remove unreachable objects
git gc                   # Garbage collection
```

## Git Flow Summary

```
main (production) ──────────────────────
  └── develop (integration) ────────────
       ├── feature/xxx ────── (merge back)
       ├── feature/yyy ────── (merge back)
       └── hotfix/zzz ──────── (merge to main + develop)
```

## Practice

1. Git aliases setup karo aur use karo for a week.
2. Cherry pick: ek commit ko dusri branch pe apply karo.
3. Pre-commit hook banao jo linting run kare.

---

**Git mastery done!** Now collaborate, contribute, ship code.


## Quick Tip

Practice makes perfect. Don't just read — write code!
