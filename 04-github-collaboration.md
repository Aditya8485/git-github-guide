# 04 — GitHub & Collaboration

## Fork & Pull Request Workflow

```
1. Fork repo (on GitHub)
2. Clone your fork locally
3. Create branch, make changes
4. Push to your fork
5. Create Pull Request on original repo
6. Discuss, review, merge
```

## Pull Requests

- Go to original repo → Pull Requests → New PR
- Describe your changes clearly
- Link issues: "Fixes #42"
- Request review from team

## Issues & Project Board

- Issues: bug reports, feature requests, tasks
- Labels: bug, enhancement, help wanted
- Projects: Kanban board for task management
- Milestones: group issues by release/version

## GitHub Profile README

Create a repo named same as your username → `README.md` = profile bio!

```markdown
# Your Name

Software Developer | Open Source Contributor

- Currently learning: React, Node.js
- Fun fact: I make my contribution graph green for fun
```

## SSH Setup

```bash
ssh-keygen -t ed25519 -C "your@email.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
# Add public key to GitHub Settings → SSH Keys
git remote set-url origin git@github.com:user/repo.git
```

## GitHub CLI (gh)

```bash
gh repo create my-project --public
gh pr create --title "Add feature" --body "Description"
gh issue list
gh issue create --title "Bug" --body "Details"
```

## Practice

1. Kisi open source repo ko fork karo, ek improvement karo, PR banao.
2. Apna profile README banao GitHub pe.
3. GitHub CLI install karo aur repo create karo via CLI.

---
*Next: 05-advanced-tips.md →*


## Additional Note

Added some more thoughts on this topic.


## Resources

- [Official Docs](https://docs.example.com)
- [Tutorial](https://tutorial.example.com)


## Additional Note

Added some more thoughts on this topic.


<!-- TODO: add more examples here -->


## Additional Note

Added some more thoughts on this topic.


## Additional Note

Added some more thoughts on this topic.
