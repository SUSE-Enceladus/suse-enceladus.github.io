---
layout: page
title: Using Git
subtitle: A small Git primer
---

# Git Configuration

## Add email and name to global config

```
git config --global user.name "Full Name"
git config --global user.email email@example.com
```

## Set default editor (optional)

The editor is used to edit commit messages and when rebasing commits.
If not set the default visual editor for the system will be used.

```
git config --global core.editor vim
```

## Create PGP key for signing commits and add public key to GitHub account

Note: This should be a new key only for Git commits.

https://help.github.com/articles/generating-a-new-gpg-key/

Recommend adding a note to the key such as "(Git signing key)"

https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work


## Set PGP signing key

```
git config --global user.signingkey {signing-key-fingerprint}
```

## Autosign all commits by default

```
git config --global commit.gpgsign true
```

## Confirm configuration

Default location for global config is: ~/.gitconfig

```
git config --list
```

## Add SSH key to GitHub

https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

# Project Workflow

## Clone repo locally

If SSH public key has been added to GitHub then you can clone using SSH.

```
git clone git@github.com:SUSE-Enceladus/ec2imgutils.git
```

Or to clone into an existing directory:

```
git clone git@github.com:SUSE-Enceladus/openbare.git openbare/
```

## Checkout master branch

```
git checkout master
```

## Checkout a new branch from master.

All changes should be made in a feature branch and merged through
reviewed pull requests.

```
git checkout -b {branch-name}
```

Branch name should be short but descriptive.

## Stage a new file

```
git add {file-name}
```

## Commit changes

`-a` automagically stages files that have been deleted and modified

```
git commit -a
```

## Push commits & branch upstream

`-u` pushes the new branch upstream

```
git push -u origin {branch-name}
```

## Push commits upstream

```
git push
```

# Other

- Commit messages: https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
- GitHub tutorial: https://try.github.io/levels/1/challenges/1
- Bash Git Status: https://github.com/magicmonty/bash-git-prompt
