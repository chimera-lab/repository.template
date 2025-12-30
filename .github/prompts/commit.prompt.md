---
agent: repository-manager
description: Execute SSH key setup and perform git operations with submodule sync.
---

# /commit - Git Commit and Push with Submodules

## :book: Table of content

(#agent-repository-manager-description-execute-ssh-key-setup-and-perform-git-operations-with-submodule-sync)
- [Table of content](#table-of-content)
- [1. Verify SSH Access](#1-verify-ssh-access)
- [2. SSH Key Setup](#2-ssh-key-setup)
- [3. Git Operations](#3-git-operations)
- [Expected Output](#expected-output)
- [Error Handling](#error-handling)

## 1. Verify SSH Access

Check if SSH is accessible:

- Test connection: `ssh -T git@github.com`
- If fails, check terminal history for previous SSH setup commands

## :gear: 2. SSH Key Setup

If the SSH access steps failt, show one line execution for:

- Eval ssh socket: `eval "$(ssh-agent -s)"`
- Add SSH key with "github" in name: `ssh-add ~/.ssh/*github.com`

## 3. Git Operations

Using `git` and `git submodule --recursive` for faster execution:

1. **Check for changes**: `git status` and `git submodule foreach --recursive 'git status'`
   - If no submodule changes detected, skip all submodule operations (fetch, pull, push)
2. **Fetch and prune**: `git fetch --prune` and `git submodule foreach --recursive 'git fetch --prune'`
3. **Pull changes**: `git pull` and `git submodule foreach --recursive 'git pull'`
4. **Analyze changes**: Review all changes in main repo and submodules, list modified files by type
5. **Create logical commit groups**: Group related changes together using conventional commit format
6. **Stage and commit**: For each logical group, stage files and create a commit with appropriate conventional commit message
7. **Push**: `git push` and `git submodule foreach --recursive 'git push'`

## Expected Output

- SSH agent PID confirmation
- Identity file added confirmation
- Git status for main repo and all submodules
- Fetch, pull, commit, and push results
- Success/failure messages for each operation

## Error Handling

- Continue execution even if submodules have no changes
- Report any failed operations
- Verify SSH key is loaded before proceeding
