---
name: git-ds-store-cleaner
description: Configures Git to globally ignore macOS .DS_Store files and removes them from existing repository caches. Use when a user needs to stop .DS_Store files from being tracked, clean up a cluttered repository, or configure global git ignore settings.
---

# Git DS_Store Cleaner

This skill handles the global blocking and removal of macOS `.DS_Store` files from Git repositories.

## Capability 1: Configure Global Ignore

Use this workflow to prevent `.DS_Store` files from being tracked in *any* future repository on the machine.

```bash
# 1. Create a global exclusion list
echo ".DS_Store" >> ~/.gitignore_global

# 2. Configure Git to use this exclusion list
git config --global core.excludesfile ~/.gitignore_global
```
