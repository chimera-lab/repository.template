______________________________________________________________________

## :white_check_mark: agent: project-manager description: Recover and restore the todo list from previous context or conversation

# :white_check_mark: /recover-task - Recover Todo List

## :book: Table of Contents

- [:white_check_mark: /recover-task - Recover Todo List](#whitecheckmark-recover-task---recover-todo-list)
  - [:book: Table of Contents](#book-table-of-contents)
  - [:white_check_mark: agent: project-manager description: Recover and restore the todo list from previous context or conversation](#whitecheckmark-agent-project-manager-description-recover-and-restore-the-todo-list-from-previous-context-or-conversation)
  - [:book: Table of content](#book-table-of-content)
  - [:book: Table of content](#book-table-of-content)
  - [Execution Steps](#execution-steps)
  - [Recovery Sources (Priority Order)](#recovery-sources-priority-order)
  - [Expected Output](#expected-output)
  - [Error Handling](#error-handling)

## :book: Table of content

- [Table of content](#table-of-content)
  - [agent: project-manager
    description: Recover and restore the todo list from previous context or conversation](#agent-project-manager-description-recover-and-restore-the-todo-list-from-previous-context-or-conversation)
- [:white_check_mark: /recover-task - Recover Todo List](#whitecheckmark-recover-task---recover-todo-list)
  - [:book: Table of content](#book-table-of-content)
  - [Execution Steps](#execution-steps)
  - [Recovery Sources (Priority Order)](#recovery-sources-priority-order)
  - [Expected Output](#expected-output)
  - [Error Handling](#error-handling)

## :book: Table of content

- [agent: project-manager
  description: Recover and restore the todo list from previous context or conversation](#agent-project-manager-description-recover-and-restore-the-todo-list-from-previous-context-or-conversation)
- [Table of content](#table-of-content)
- [Execution Steps](#execution-steps)
- [Recovery Sources (Priority Order)](#recovery-sources-priority-order)
- [Expected Output](#expected-output)
- [Error Handling](#error-handling)

## Execution Steps

1. **Analyze Context**

   - Review conversation history for previous todo list states
   - Check for any saved todo states in recent messages
   - Identify the last valid todo list configuration

1. **Validate Todo Structure**

   - Ensure all recovered todos have valid structure:
     - id (sequential numbers)
     - title (concise, action-oriented)
     - description (detailed context)
     - status (not-started, in-progress, completed)
   - Check for any incomplete or corrupted entries

1. **Restore Todo List**

   - Use `manage_todo_list` tool with operation="write"
   - Include all recovered todos with their original status
   - Preserve the work progress and context

1. **Report Recovery**

   - Confirm successful recovery
   - Show summary of recovered todos by status:
     - Completed tasks count
     - In-progress tasks (should be 0 or 1)
     - Not-started tasks count
   - Highlight any todos that need attention

## Recovery Sources (Priority Order)

1. Last `manage_todo_list` operation in conversation
1. Explicit todo mentions in recent messages
1. Infer from completed work and pending requests

## Expected Output

- Confirmation of todo list restoration
- Summary table showing all todos with their status
- Next suggested action based on recovered state

## Error Handling

- If no previous todo list found: Report this and ask if user wants to create new list
- If corrupted data found: Report issues and ask for clarification
- If multiple versions found: Use the most recent complete version
