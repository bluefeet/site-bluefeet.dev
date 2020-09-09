---
title: Dev Setup
icon: 🦓
---

## Shortcuts

| OS | App | Keys | Detail |
|-|-|-|-|
| Windows | vscode | F2 | Rename the symbol at the cursor. |
| Windows | vscode | Ctrl-Shift-P | Command pallette. |

## Shell Aliases

These are my most used aliases from [oh my zsh](https://ohmyz.sh/) which I've also back-ported into my bash setup for those times that I'm on a system without zsh.

| Alias | Command |
|-|-|
| `ga` | `git add` |
| `gapa` | `git add --patch` |
| `gbl` | `git blame -b -w` |
| `gcm` | `git checkout $(git_main_branch)` |
| `gcmsg` | `git commit -m` |
| `gco` | `git checkout` |
| `gd` | `git diff` |
| `gdca` | `git diff --cached` |
| `gdw` | `git diff --word-diff` |
| `gf` | `git fetch` |
| `gp` | `git push` |
| `gpf` | `git push --force-with-lease` |
| `gpf!` | `git push --force` |
| `grb` | `git rebase` |
| `grbm` | `git rebase $(git_main_branch)` |
| `groh` | `git reset origin/$(git_current_branch) --hard` |
| `gsh` | `git show` |
| `gss` | `git status -s` |
| `gsta` | `git stash save` |
| `gstp` | `git stash pop` |
| `gup` | `git pull --rebase` |
| `gupa` | `git pull --rebase --autostash` |
| `gwch` | `git whatchanged -p --abbrev-commit --pretty=medium` |
| `gwip` | `git add -A; git rm $(git ls-files --deleted) 2> /dev/null; git commit --no-verify --no-gpg-sign -m "--wip-- [skip ci]"` |
