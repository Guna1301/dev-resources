# Git Cheat Sheet
A practical reference for common Git commands and workflows.

---

## Basics
| Command | Description |
|---------|-------------|
| `git status` | Show current branch and staged changes |
| `git add <file>` | Stage file(s) for commit |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Commit staged changes with a message |
| `git log --oneline --graph --all` | View commit history |

---

## Branching
| Command | Description |
|---------|-------------|
| `git branch` | List local branches |
| `git branch -a` | List all branches (local + remote) |
| `git checkout <branch>` | Switch branch |
| `git checkout -b <branch>` | Create and switch to a new branch |
| `git merge <branch>` | Merge branch into current branch |
| `git rebase <branch>` | Rebase current branch onto another branch |

---

## Undo Changes
| Command | Description |
|---------|-------------|
| `git restore <file>` | Discard changes in working directory |
| `git restore --staged <file>` | Unstage a file |
| `git reset --hard <commit>` | Reset working directory and staging area |
| `git revert <commit>` | Revert a commit with a new commit |

---

## Remote Repositories
| Command | Description |
|---------|-------------|
| `git remote -v` | Show configured remotes |
| `git remote add upstream <url>` | Add original repo as upstream |
| `git fetch upstream` | Fetch changes from upstream |
| `git pull origin main` | Pull latest changes from remote |
| `git push origin <branch>` | Push branch to remote repository |

---

## Tips & Shortcuts
- `git commit -am "msg"` → Stage + commit in one command (for tracked files)
- `git log --oneline --graph` → Visual commit history
- Always work on a **feature branch**, not `main`.
- Pull latest changes before starting new work to avoid conflicts.
