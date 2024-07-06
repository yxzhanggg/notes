---
layout: post
title:  Git and Github quick start
date:   2022-08-26
---

# Configure Github
```sh
# Configure local git
git config --global user.name "<name>"
git config --global user.email "<email>"
git config --global core.editor "vim"

# Generate ssh file
ssh-keygen -t rsa
# Copy everything in `~/.ssh/id_rsa.pub` to SSH setting of your account

# Test connection
ssh -T git@github.com
```
