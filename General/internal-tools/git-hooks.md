<!--
START OF: git-hooks.md
Purpose: Outlines the Git hooks in use and their responsibilities.
Update Frequency: Update this when a new hook is added or behavior is modified.
Location: docs/internal-tools/git-hooks.md
-->

# Git Hooks

## Purpose

Automate checks and enforce standards before Git operations are completed (e.g., before commits or pushes).

---

## Active Hooks

| Hook         | Trigger Event       | Function                                    |
|--------------|---------------------|---------------------------------------------|
| `pre-commit` | Before `git commit` | Lint and format staged files                |
| `pre-push`   | Before `git push`   | Run unit tests and validate commit messages |
| `commit-msg` | On commit message   | Enforces commit message structure           |

---

## Setup

```bash
./setup-git-hooks.sh
Hooks are installed into .git/hooks and symlinked to our hooks/ directory.
```

---

## Commit Message Format

[type]: short description

[optional longer description]

Valid types: feat, fix, docs, refactor, chore, test

---

## Notes

- Built using Husky or custom Bash scripts.
- Extendable for team needs.

<!-- END OF: git-hooks.md -->
