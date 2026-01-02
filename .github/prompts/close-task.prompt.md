---
name: close-task
agent: repository-manager
description: Close a task and commit with optional issue reference
---

# :file_folder: Close Task

## :book: Table of Contents

- [:file\_folder: Close Task](#file_folder-close-task)
  - [:world\_map: Task Closure](#world_map-task-closure)
    - [:compass: Verify Task Completion](#compass-verify-task-completion)
    - [:compass: Commit Changes](#compass-commit-changes)
    - [:compass: Push and Verify](#compass-push-and-verify)
  - [:world\_map: Output](#world_map-output)

## :world_map: Task Closure

### :compass: Verify Task Completion

- Check git status: `git status`
- Review all changes are ready
- Identify issue number if applicable


### :compass: Commit Changes

- Stage all: `git add .`
- Conventional format: `{type}: {description}`
- Add issue reference: `Closes #{number}`
- Types: feat, fix, docs, style, refactor, test, chore


### :compass: Push and Verify

- Push: `git push`
- Verify closure: `gh issue view {number}`
- Update todo: `manage_todo_list` tool


## :world_map: Output

- Commit hash and message
- Push confirmation
- Issue status (if applicable)
