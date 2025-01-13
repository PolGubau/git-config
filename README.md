# Git Configuration Guide

This document explains the Git configuration settings used in this repository and how they optimize workflows. Below is a detailed description of each section in the configuration file.

---

## [core]
- **autocrlf = true**: Ensures proper handling of line endings across different operating systems.
- **ignorecase = false**: Makes Git case-sensitive, useful for case-sensitive file systems.
- **preloadIndex = true**: Improves performance for large repositories by preloading the index.
- **fileMode = false**: Prevents Git from tracking file permission changes.
- **sshCommand**: Specifies the SSH command to use (`OpenSSH`).

---

## [user]
- **email**: Specifies the author’s email.
- **name**: Sets the author’s full name (used for commits).

---

## [fetch]
- **prune = true**: Automatically removes stale references to remote branches.

---

## [commit]
- **template = ~/.gitmessage.txt**: Sets a default commit message template. Use it to enforce consistent commit formatting.

---

## [filter "lfs"]
Git LFS configuration to handle large files efficiently:
- **smudge**: Expands LFS files when checked out.
- **process**: Processes files through LFS.
- **required**: Ensures LFS is required.
- **clean**: Cleans files before committing.

---

## [credential]
- **helper = store**: Saves credentials locally for easier authentication.

---

## [alias]
Custom Git aliases to simplify commands and enhance productivity:

### Commit Aliases
- **cm**: Quickly commit with a message.
- **amend**: Amend the last commit without modifying its message.
- **cam**: Commit all changes with a message.

### Checkout Aliases
- **co**: Shortcut for `checkout`.
- **cob**: Create and switch to a new branch.

### Branch Aliases
- **br**: List branches.
- **bra**: List all branches (local and remote).
- **brr**: List remote branches.
- **bd**: Delete a branch.
- **bdd**: Force delete a branch.

### Status Aliases
- **st**: Display a concise status, including branch info and ignored files.

### Pull Aliases
- **pom**: Pull from origin master.
- **pob**: Pull from the current branch.
- **poma**: Pull from origin main.
- **puf**: Pull with fast-forward only.
- **pr**: Pull with rebase.

### Push Aliases
- **pub**: Push the current branch.
- **puf**: Push force with lease (safe force push).

### Log Aliases
- **lg**: Visualize the commit graph.
- **ll**: Display detailed log entries.
- **ll2**: More detailed log with emails.
- **llo**: One-line logs.
- **ls**: Show commit statistics.
- **lsg**: Show commit statistics with a graph.

### Diff Aliases
- **df**: Show file differences.
- **dft**: List files changed in a commit.
- **dfa**: Show staged differences.

### Rebase Aliases
- **rb**: Start a rebase.
- **rbc**: Continue a rebase.
- **rbi**: Start an interactive rebase.

### General Aliases
- **cl**: Clone a repository.
- **rv**: Show the current branch.
- **last**: Show the last commit.
- **rst**: Reset to the previous commit (soft reset).
- **hrd**: Perform a hard reset.
- **clean**: Clean untracked files.
- **undo**: Undo the last commit (soft reset).
- **unstage**: Remove files from staging.

### Tag Aliases
- **tagl**: List all tags.
- **tagd**: Delete a tag.
- **ptt**: Push all tags.

### Stash Aliases
- **stashl**: List stashes.
- **stashp**: Apply and drop the last stash.
- **stashs**: Save a new stash.
- **stashu**: Apply a stash without dropping it.

### Submodule Aliases
- **subu**: Update and initialize submodules recursively.
- **subs**: Show submodule status.
- **suba**: Add a submodule.

### Other Aliases
- **whoami**: Display the current user.
- **cfg**: List configuration settings.
- **aliases**: Display all aliases.
- **branches**: List all branches (local and remote).

---

## [diff]
- **tool = vscode**: Use Visual Studio Code as the diff tool.
- **mnemonicprefix = true**: Use mnemonic prefixes in diffs.

---

## [merge]
- **tool = vscode**: Use Visual Studio Code as the merge tool.
- **conflictstyle = diff3**: Provides better context during merge conflicts.

---

## [push]
- **default = simple**: Push the current branch by default.

---

## [rebase]
- **autosquash = true**: Automatically squashes fixup commits during an interactive rebase.
- **autostash = true**: Automatically stashes changes before a rebase.

---

## How to Use
1. Copy the above configuration into your `~/.gitconfig` file.
2. Ensure that you have the `~/.gitmessage.txt` template for commit messages.
3. Test aliases using:
   ```bash
   git aliases
   ```
4. Customize settings as per your team’s needs.

For any issues or questions, feel free to reach out!

