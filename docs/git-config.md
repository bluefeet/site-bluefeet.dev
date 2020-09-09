---
title: Git Config
icon: 🐙
---

```sh
git config --global user.name 'Aran Clary Deltac'
git config --global user.email 'bluefeet@gmail.com'
git config --global fetch.prune true
git config --global fetch.pruneTags true
git config --global push.default current
git config --global protocol.version 2
git config --global index.version 4
git config --global merge.conflictstyle diff3
git update-index --test-untracked-cache && \
  git config --global core.untrackedCache true
```
